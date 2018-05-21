---
UID: TP:powermeter
ms.assetid: 87d19931-d859-3aff-b7ce-1b0060d965a5
ms.author: windowsdriverdev
ms.date: 05/21/18
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: portal
---

# Power Metering and Budgeting Reference



Overview of the Power Metering and Budgeting Reference technology.

To develop Power Metering and Budgeting Reference, you need these headers:

 * [emi.h](..\emi\index.md)

For the programming guide, see [Power Metering and Budgeting Reference](https://review.docs.microsoft.com/en-us/win32-test/powermeter).

## Structures

| Title   | Description   |
| ---- |:---- |
| [EMI_MEASUREMENT_DATA structure](..\emi\ns-emi-emi_measurement_data.md) | The EMI_MEASUREMENT_DATA structure provides data about the current energy measurement and the time at which the measurement was taken. |
| [EMI_METADATA structure](..\emi\ns-emi-emi_metadata.md) | The EMI_METADATA structure provides metadata about a device that supports the Energy Metering Interface (EMI) interface, such as the hardware model and hardware revision. |
| [EMI_METADATA_SIZE structure](..\emi\ns-emi-emi_metadata_size.md) | The EMI_METADATA_SIZE structure specifies the size of the Energy Metering Interface (EMI) metadata object that can be obtained from the device by issuing an IOCTL_EMI_GET_METADATA request. |
| [EMI_VERSION structure](..\emi\ns-emi-emi_version.md) | The EMI_VERSION structure describes the version of the Energy Metering Interface (EMI) that is supported by a device. |

## Enumerations

| Title   | Description   |
| ---- |:---- |
| [EMI_MEASUREMENT_UNIT enumeration](..\emi\ne-emi-emi_measurement_unit.md) | The EMI_MEASUREMENT_UNIT enumeration represents the available units of energy measurements that can be retrieved from a device by using IOCTL_EMI_GET_MEASUREMENT. |

## I/O control codes

| Title   | Description   |
| ---- |:---- |
| [IOCTL_EMI_GET_MEASUREMENT IOCTL](..\emi\ni-emi-ioctl_emi_get_measurement.md) | The IOCTL_EMI_GET_MEASUREMENT control code retrieves the current energy measurement and the time at which the measurement was taken. |
| [IOCTL_EMI_GET_METADATA IOCTL](..\emi\ni-emi-ioctl_emi_get_metadata.md) | The IOCTL_EMI_GET_METADATA control code retrieves EMI metadata from a device. |
| [IOCTL_EMI_GET_METADATA_SIZE IOCTL](..\emi\ni-emi-ioctl_emi_get_metadata_size.md) | The IOCTL_EMI_GET_METADATA_SIZE control code retrieves the size of the EMI metadata object that can be obtained from the device by issuing an IOCTL_EMI_GET_METADATA request. |
| [IOCTL_EMI_GET_VERSION IOCTL](..\emi\ni-emi-ioctl_emi_get_version.md) | The IOCTL_EMI_GET_VERSION control code retrieves the current version of the EMI interface supported by the device. |
