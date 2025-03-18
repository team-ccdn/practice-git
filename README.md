# practice-git

## よく使うコマンド

### gitのバージョンを確認
```
git --version
```

### ブランチの作成
```
git branch { New Branch Name }
```

### ブランチの切り替え
```
git switch { Branch Name } / git checkout { Branch Name }
```

### ブランチを作成して切り替える
```
git checkout -b { Branch Name }
```

### 現在の作業ブランチの確認
```
git branch
```

### リモートリポジトリに作成したブランチを反映
```
git push origin { New Branch Name }
```

### ローカルブランチを削除
```
git branch --delete { Branch Name } / git branch -d { Branch Name }
```

### リモートブランチを削除
```
git push --delete origin { Branch Name } / git push origin :{ Branch Name }
```

### ローカルリポジトリの状態を確認
```
git status
```

### 特定のファイルをステージングエリアに登録
```
git add { FileName }
```

#### 変更したファイル全てをステージングエリアに登録
```
git add .
```

### ステージングエリアに登録されている特定のファイルを取り消し
```
git restore --staged { FileName }
```

#### ステージングエリアに登録されている全てのファイルを取り消し
```
git restore --staged .
```

### コミットせずに変更を待避
```
git stash -u
```

#### 待避した作業の一覧
```
git stash list
```

#### 待避した作業を元に戻す
```
git stash apply stash@{{ Number }}
```

### ステージングエリアに登録されているファイルをコミット
```
git commit
```

#### Vimが立ち上がる場合
ノーマルモードから`i`でインサートモードに入り、コミットメッセージ入力後`esc`でノーマルモードに戻り、`:wq`で保存して終了  
コミットメッセージの入力をキャンセルしたい場合は、ノーマルモードで`:q!`で保存せずに終了

### ステージングエリアに登録されているファイルをコミットメッセージ付きでコミット
```
git commit - "{ Commit Message }"
```
※Vimは立ち上がらない

### 直前のコミットを取り消す
```
git reset --soft 'HEAD^'
```

### プッシュする
```
git push
```
