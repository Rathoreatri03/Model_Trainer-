# Model Trainer

Model Trainer is a Python package designed to simplify the process of training YOLO (You Only Look Once) models for object detection tasks. With Model Trainer, users can easily train YOLO models using custom datasets and split their data into training, validation, and testing sets. The package provides classes for both model training and data splitting, allowing users to efficiently manage their training pipeline. Additionally, Model Trainer includes functionality for saving the best-performing model weights, making it easy to deploy trained models for inference tasks.

## Features

- Train YOLO models with custom datasets
- Split datasets into training, validation, and testing sets
- Save best-performing model weights for deployment

## Installation

You can install Model Trainer using pip:

```bash
pip install Model_Trainer
```

## Usage

### Training a YOLO Model

```python
from Model_Trainer import YOLO_Trainer

# Initialize YOLO Trainer with data.yaml folder path and destination folder for best weights
trainer = YOLO_Trainer(Data_yaml_fold_path='path/to/data.yaml', Best_Weight_dest='path/to/destination', epochs=50)

# Select YOLO model version and configuration
trainer.model_selection()

# Train the selected model
trainer.model_training()

# Save the best-performing model weights
trainer.model_saving()
```

### Splitting Data

```python
from Model_Trainer import Data_Splitter

# Initialize Data Splitter with data folder, destination folder, and number of classes
splitter = Data_Splitter(data_folder='path/to/data', dest_fold='path/to/destination', no_classes=3)

# Collect paths and names of classes
splitter.class_path_folder()

# Split the data into train, validation, and test sets
splitter.split()
```

## License

Model Trainer is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.



## Support

For support, please open an issue on our [GitHub repository](https://github.com/yourusername/Model_Trainer/issues).