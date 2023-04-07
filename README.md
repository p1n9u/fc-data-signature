# fc-data-signature

```bash
git clone --recurse-submodules https://github.com/p1n9u/fc-data-signature.git
```

### 기존 코드 변경 내역

```python
model = models.resnet50(pretrained=True) -> model = models.resnet50(weights='ResNet50_Weights.DEFAULT')
```

### 학습 후 유의 사항

```python
torch.save(model.state_dict(), f'best_checkpoint_epoch_{epoch + 1}.pth')
...
model_path = 'best_checkpoint_epoch_*.pth'
```
- best_checkpoint_epoch_*.pth : 변경 후 실행
