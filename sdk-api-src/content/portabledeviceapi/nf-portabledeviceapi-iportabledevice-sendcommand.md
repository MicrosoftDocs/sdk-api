---
UID: NF:portabledeviceapi.IPortableDevice.SendCommand
title: IPortableDevice::SendCommand (portabledeviceapi.h)
description: The SendCommand method sends a command to the device and retrieves the results synchronously.
helpviewer_keywords: ["IPortableDevice interface [Windows Portable Devices SDK]","SendCommand method","IPortableDevice.SendCommand","IPortableDevice::SendCommand","IPortableDeviceSendCommand","SendCommand","SendCommand method [Windows Portable Devices SDK]","SendCommand method [Windows Portable Devices SDK]","IPortableDevice interface","portabledeviceapi/IPortableDevice::SendCommand","wpdsdk.iportabledevice_sendcommand"]
old-location: wpdsdk\iportabledevice_sendcommand.htm
tech.root: wpdsdk
ms.assetid: ccc7f87a-dea3-4a1e-a181-86928e23bd35
ms.date: 12/05/2018
ms.keywords: IPortableDevice interface [Windows Portable Devices SDK],SendCommand method, IPortableDevice.SendCommand, IPortableDevice::SendCommand, IPortableDeviceSendCommand, SendCommand, SendCommand method [Windows Portable Devices SDK], SendCommand method [Windows Portable Devices SDK],IPortableDevice interface, portabledeviceapi/IPortableDevice::SendCommand, wpdsdk.iportabledevice_sendcommand
req.header: portabledeviceapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPortableDevice::SendCommand
 - portabledeviceapi/IPortableDevice::SendCommand
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - PortableDeviceGUIDs.lib
 - PortableDeviceGUIDs.dll
api_name:
 - IPortableDevice.SendCommand
---

# IPortableDevice::SendCommand


## -description

The <b>SendCommand</b> method sends a command to the device and retrieves the results synchronously.

## -parameters

### -param dwFlags [in]

Currently not used; specify zero.

### -param pParameters [in]

Pointer to an <a href="/windows/desktop/wpd_sdk/iportabledevicevalues">IPortableDeviceValues</a> interface that specifies the command and parameters to call on the device. This interface must include the following two values to indicate the command. Additional parameters vary depending on the command. For a list of the parameters that are required for each command, see <a href="/windows/desktop/wpd_sdk/commands">Commands</a>.
            

<table>
<tr>
<th>Command or property</th>
<th>Description</th>
</tr>
<tr>
<td>WPD_PROPERTY_COMMON_COMMAND_CATEGORY</td>
<td>The category <b>GUID</b> of the command to send. For example, to reset a device, you would send <b>WPD_COMMAND_COMMON_RESET_DEVICE.fmtid</b>.</td>
</tr>
<tr>
<td>WPD_PROPERTY_COMMON_COMMAND_ID</td>
<td>The PID of the command to send. For example, to reset a device, you would send <b>WPD_COMMAND_COMMON_RESET_DEVICE.pid</b>.</td>
</tr>
</table>

### -param ppResults [out]

Address of a variable that receives a pointer to an <a href="/windows/desktop/wpd_sdk/iportabledevicevalues">IPortableDeviceValues</a> interface that indicates the results of the command results, including success or failure, and any command values returned by the device. The caller must release this interface when it is done with it. The retrieved values vary by command; see the appropriate command documentation in <a href="/windows/desktop/wpd_sdk/commands">Commands</a> to learn what values are returned by each command call.

## -returns

The returned value indicates success or failure to send a command and return a result from the driver; it does not indicate whether the driver supports the command or if it encountered some error in processing the command. (For more information, see Remarks.) These errors are returned in the <b>HRESULT</b> values of the <i>ppResults</i> parameter. The possible <b>HRESULT</b> values returned by this method include, but are not limited to, those in the following table.
          

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The command was successfully received by the driver. This does not indicate that the command itself succeeded—you must check <i>ppResults</i> to determine the success or failure of the command.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
At least one of the arguments was a NULL pointer.

</td>
</tr>
</table>

## -remarks

This function is used to send a command directly to the driver. A command is a <b>PROPERTYKEY</b> that is sent to the driver to indicate the expected action, along with a list of required parameters. Each command has a list of required and optional parameters and results that must be packaged with the command for the driver to perform the requested action. A list of commands defined by Windows Portable Devices, with the required parameters and return values, is given in <a href="/windows/desktop/wpd_sdk/commands">Commands</a>.
      

Most Windows Portable Devices methods actually work by sending one or more of the Windows Portable Devices commands for you and wrapping the parameters for you. Some commands have no corresponding Windows Portable Devices methods. The only way to call these commands is by using <b>SendCommand</b>. The following commands have no corresponding method:
      

<ul>
<li>
<a href="/windows/desktop/wpd_sdk/wpd-command-common-reset-device-command">WPD_COMMAND_COMMON_RESET_DEVICE</a>
</li>
<li>
<a href="/windows/desktop/wpd_sdk/wpd-command-device-hints-get-content-location-command">WPD_COMMAND_DEVICE_HINTS_GET_CONTENT_LOCATION</a>
</li>
<li>
<a href="/windows/desktop/wpd_sdk/wpd-command-sms-send-command">WPD_COMMAND_SMS_SEND</a>
</li>
<li>
<a href="/windows/desktop/wpd_sdk/wpd-command-still-image-capture-initiate-command">WPD_COMMAND_STILL_IMAGE_CAPTURE_INITIATE</a>
</li>
<li>
<a href="/windows/desktop/wpd_sdk/wpd-command-storage-eject-command">WPD_COMMAND_STORAGE_EJECT</a>
</li>
</ul>
You also must call <b>SendCommand</b> to send any custom driver commands driver.
      

Some custom commands may require a specific Input/Output Control Code (IOCTL) access level. Your application sets this access level by calling the <a href="/windows/desktop/wpd_sdk/iportabledevicevalues-setunsignedintegervalue">IPortableDeviceValues::SetUnsignedIntegerValue</a> method on the command parameters that it passes to the <b>SendCommand</b> method. For example, if a custom command requires read-only access, you would call <b>SetUnsignedIntegerValue</b> and pass WPD_API_OPTION_IOCTL_ACCESS as the first argument and FILE_READ_ACCESS as the second argument. By updating these command parameters, your application ensures that the Windows Portable Devices API issues the command with the read-only IOCTL.
      

Errors that are encountered by the driver while processing a command are retrieved by the <i>ppResults</i> parameter, not by the <b>SendCommand</b> return value. The return value of this method is any error (or success) code that is encountered while sending the command to the driver.
      

If a driver does not support the specified command, this method will succeed, but the only guaranteed element in the returned <i>ppResults</i> parameter will be WPD_PROPERTY_COMMON_HRESULT, which will contain E_NOTIMPL. You can verify whether a driver supports a command by calling <a href="/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledevicecapabilities-getsupportedcommands">IPortableDeviceCapabilities::GetSupportedCommands</a> before calling a command.
      

If a command supports options (such as delete recursively or delete nonrecursively), you can query for supported options by calling <a href="/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledevicecapabilities-getcommandoptions">IPortableDeviceCapabilities::GetCommandOptions</a>.
      

There is no option to set a timeout in a call to <b>SendCommand</b> but the developer can attempt to cancel the command by calling <a href="/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledevice-cancel">IPortableDevice::Cancel</a> from a separate thread.


#### Examples


```cpp

// 

void ResetDevice(IPortableDevice* pDevice)
{
    HRESULT  hr = S_OK;
    CComPtr<IPortableDeviceValues>  pDevValues;

    hr = CoCreateInstance(CLSID_PortableDeviceValues,
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_IPortableDeviceValues,
        (VOID**) &pDevValues);
    if (SUCCEEDED(hr))
    {
        if (pDevValues != NULL)
        {
            hr = pDevValues->SetGuidValue(WPD_PROPERTY_COMMON_COMMAND_CATEGORY, 
                WPD_COMMAND_COMMON_RESET_DEVICE.fmtid);
            if (FAILED(hr))
            {
                printf("! IPortableDeviceValues::SetGuidValue failed, hr= 0x%lx\n", hr);
            }
            hr = pDevValues->SetUnsignedIntegerValue(WPD_PROPERTY_COMMON_COMMAND_ID,
                WPD_COMMAND_COMMON_RESET_DEVICE.pid);
            if (FAILED(hr))
            {
                printf("! IPortableDeviceValues::SetGuidValue failed, hr= 0x%lx\n", hr);
            }
        }
    }
    hr = pDevice->SendCommand(0, pDevValues, &pDevValues);
    if (FAILED(hr))
    {
        printf("! Failed to reset the device, hr = 0x%lx\n",hr);
    }
    else
        printf("Device successfully reset\n");
    return;
}

//

```

## -see-also

<a href="/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevice">IPortableDevice Interface</a>