---
UID: TP:deviceaccess
ms.assetid: c4afd78e-1e89-3dda-9c6f-6a2002ebabca
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: 
ms.prod: windows
ms.technology: windows-sdk
ms.topic: portal
archived: true
---

# Device Access API



Overview of the Device Access API technology.

To develop Device Access API, you need these headers:

 * [deviceaccess.h](..\deviceaccess\index.md)

For the programming guide, see [Device Access API](/previous-versions/windows/desktop/deviceaccess).

## Functions

| Title   | Description   |
| ---- |:---- |
| [CreateDeviceAccessInstance function](..\deviceaccess\nf-deviceaccess-createdeviceaccessinstance.md) | Creates the object that's used to access a device. The instantiated object implements the IDeviceIoControl and ICreateDeviceAccessAsync interfaces. |

## Interfaces

| Title   | Description   |
| ---- |:---- |
| [ICreateDeviceAccessAsync interface](..\deviceaccess\nn-deviceaccess-icreatedeviceaccessasync.md) | The ICreateDeviceAccessAsync interface is returned from a call to CreateDeviceAccessInstance. |
| [IDeviceIoControl interface](..\deviceaccess\nn-deviceaccess-ideviceiocontrol.md) | Sends a control code to a device driver.This action causes the device to perform the corresponding operation. |
| [IDeviceRequestCompletionCallback interface](..\deviceaccess\nn-deviceaccess-idevicerequestcompletioncallback.md) | Provides a method to handle the completion of calls to the DeviceIoControlAsyncmethod. |

## Methods

| Title   | Description   |
| ---- |:---- |
| [ICreateDeviceAccessAsync::Cancel](..\deviceaccess\nf-deviceaccess-icreatedeviceaccessasync-cancel.md) | The Cancel method attempts to cancel an asynchronous operation that is in progress. |
| [ICreateDeviceAccessAsync::Close](..\deviceaccess\nf-deviceaccess-icreatedeviceaccessasync-close.md) | The Close method performs cleanup after the asynchronous operation is completed and you retrieve the results. |
| [ICreateDeviceAccessAsync::GetResult](..\deviceaccess\nf-deviceaccess-icreatedeviceaccessasync-getresult.md) | Retrieves an IDeviceIoControl object that's bound to the device interface that's specified in a call to the CreateDeviceAccessInstance function. |
| [ICreateDeviceAccessAsync::Wait](..\deviceaccess\nf-deviceaccess-icreatedeviceaccessasync-wait.md) | The Wait method waits a specified length of time for an asynchronous bind operation that is in progress to finish. |
| [IDeviceIoControl::CancelOperation](..\deviceaccess\nf-deviceaccess-ideviceiocontrol-canceloperation.md) | The CancelOperation method attempts to cancel a previously issued call by using the DeviceIoControlAsync method. |
| [IDeviceIoControl::DeviceIoControlAsync](..\deviceaccess\nf-deviceaccess-ideviceiocontrol-deviceiocontrolasync.md) | The DeviceIoControlAsync method sends an asynchronous device input/output (I/O) control request to the device interface that the call to the CreateDeviceAccessInstance function specified. |
| [IDeviceIoControl::DeviceIoControlSync](..\deviceaccess\nf-deviceaccess-ideviceiocontrol-deviceiocontrolsync.md) | The DeviceIoControlSync method sends a synchronous device input/output (I/O) control request to the device interface that the call to the CreateDeviceAccessInstance function specified. |
| [IDeviceRequestCompletionCallback::RequestCompletion](..\deviceaccess\nf-deviceaccess-idevicerequestcompletioncallback-requestcompletion.md) | Implement the RequestCompletion method to handle the completion of calls to the DeviceIoControlAsyncmethod. |
