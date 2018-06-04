---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IPortableDevice::SendCommand


## -description



        The <b>SendCommand</b> method sends a command to the device and retrieves the results synchronously.
      


## -parameters




### -param dwFlags [in]


            Currently not used; specify zero.
          


### -param pParameters [in]


            Pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff597597">IPortableDeviceValues</a> interface that specifies the command and parameters to call on the device. This interface must include the following two values to indicate the command. Additional parameters vary depending on the command. For a list of the parameters that are required for each command, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff597554">Commands</a>.
            

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


            Address of a variable that receives a pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff597597">IPortableDeviceValues</a> interface that indicates the results of the command results, including success or failure, and any command values returned by the device. The caller must release this interface when it is done with it. The retrieved values vary by command; see the appropriate command documentation in <a href="https://msdn.microsoft.com/library/windows/hardware/ff597554">Commands</a> to learn what values are returned by each command call.
          


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




        This function is used to send a command directly to the driver. A command is a <b>PROPERTYKEY</b> that is sent to the driver to indicate the expected action, along with a list of required parameters. Each command has a list of required and optional parameters and results that must be packaged with the command for the driver to perform the requested action. A list of commands defined by Windows Portable Devices, with the required parameters and return values, is given in <a href="https://msdn.microsoft.com/library/windows/hardware/ff597554">Commands</a>.
      


        Most Windows Portable Devices methods actually work by sending one or more of the Windows Portable Devices commands for you and wrapping the parameters for you. Some commands have no corresponding Windows Portable Devices methods. The only way to call these commands is by using <b>SendCommand</b>. The following commands have no corresponding method:
      

<ul>
<li>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff597754">WPD_COMMAND_COMMON_RESET_DEVICE</a>
</li>
<li>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff597756">WPD_COMMAND_DEVICE_HINTS_GET_CONTENT_LOCATION</a>
</li>
<li>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff597828">WPD_COMMAND_SMS_SEND</a>
</li>
<li>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff597829">WPD_COMMAND_STILL_IMAGE_CAPTURE_INITIATE</a>
</li>
<li>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff597830">WPD_COMMAND_STORAGE_EJECT</a>
</li>
</ul>

        You also must call <b>SendCommand</b> to send any custom driver commands driver.
      


        Some custom commands may require a specific Input/Output Control Code (IOCTL) access level. Your application sets this access level by calling the <a href="https://msdn.microsoft.com/9b5d1b8c-7863-4807-a34b-56d30a47bd5c">IPortableDeviceValues::SetUnsignedIntegerValue</a> method on the command parameters that it passes to the <b>SendCommand</b> method. For example, if a custom command requires read-only access, you would call <b>SetUnsignedIntegerValue</b> and pass WPD_API_OPTION_IOCTL_ACCESS as the first argument and FILE_READ_ACCESS as the second argument. By updating these command parameters, your application ensures that the Windows Portable Devices API issues the command with the read-only IOCTL.
      


        Errors that are encountered by the driver while processing a command are retrieved by the <i>ppResults</i> parameter, not by the <b>SendCommand</b> return value. The return value of this method is any error (or success) code that is encountered while sending the command to the driver.
      


        If a driver does not support the specified command, this method will succeed, but the only guaranteed element in the returned <i>ppResults</i> parameter will be WPD_PROPERTY_COMMON_HRESULT, which will contain E_NOTIMPL. You can verify whether a driver supports a command by calling <a href="https://msdn.microsoft.com/974b16c7-27a0-40a6-8941-e93293a69b48">IPortableDeviceCapabilities::GetSupportedCommands</a> before calling a command.
      


        If a command supports options (such as delete recursively or delete nonrecursively), you can query for supported options by calling <a href="https://msdn.microsoft.com/d222968f-3ca7-4a4d-bdc6-89a6ca98c7b0">IPortableDeviceCapabilities::GetCommandOptions</a>.
      

There is no option to set a timeout in a call to <b>SendCommand</b> but the developer can attempt to cancel the command by calling <a href="https://msdn.microsoft.com/dcda2e43-ee12-44a4-a7ab-a2a542082d07">IPortableDevice::Cancel</a> from a separate thread.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
// 

void ResetDevice(IPortableDevice* pDevice)
{
    HRESULT  hr = S_OK;
    CComPtr&lt;IPortableDeviceValues&gt;  pDevValues;

    hr = CoCreateInstance(CLSID_PortableDeviceValues,
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_IPortableDeviceValues,
        (VOID**) &amp;pDevValues);
    if (SUCCEEDED(hr))
    {
        if (pDevValues != NULL)
        {
            hr = pDevValues-&gt;SetGuidValue(WPD_PROPERTY_COMMON_COMMAND_CATEGORY, 
                WPD_COMMAND_COMMON_RESET_DEVICE.fmtid);
            if (FAILED(hr))
            {
                printf("! IPortableDeviceValues::SetGuidValue failed, hr= 0x%lx\n", hr);
            }
            hr = pDevValues-&gt;SetUnsignedIntegerValue(WPD_PROPERTY_COMMON_COMMAND_ID,
                WPD_COMMAND_COMMON_RESET_DEVICE.pid);
            if (FAILED(hr))
            {
                printf("! IPortableDeviceValues::SetGuidValue failed, hr= 0x%lx\n", hr);
            }
        }
    }
    hr = pDevice-&gt;SendCommand(0, pDevValues, &amp;pDevValues);
    if (FAILED(hr))
    {
        printf("! Failed to reset the device, hr = 0x%lx\n",hr);
    }
    else
        printf("Device successfully reset\n");
    return;
}

//
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/98c48e56-56b8-4800-b52b-ac08f2abf27e">IPortableDevice Interface</a>
 

 

