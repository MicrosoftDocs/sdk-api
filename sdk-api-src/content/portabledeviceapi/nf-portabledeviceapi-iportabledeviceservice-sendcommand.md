---
UID: NF:portabledeviceapi.IPortableDeviceService.SendCommand
title: IPortableDeviceService::SendCommand (portabledeviceapi.h)
author: windows-sdk-content
description: Sends a standard WPD command and its parameters to the service.
old-location: wpdsdk\iportabledeviceservice_sendcommand.htm
tech.root: wpd_sdk
ms.assetid: c6c42347-145c-4be7-bea6-34b13c211cb1
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IPortableDeviceService interface [Windows Portable Devices SDK],SendCommand method, IPortableDeviceService.SendCommand, IPortableDeviceService::SendCommand, SendCommand, SendCommand method [Windows Portable Devices SDK], SendCommand method [Windows Portable Devices SDK],IPortableDeviceService interface, portabledeviceapi/IPortableDeviceService::SendCommand, wpdsdk.iportabledeviceservice_sendcommand
ms.topic: method
req.header: portabledeviceapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: PortableDeviceAPI.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - PortableDeviceAPI.h
api_name:
 - IPortableDeviceService.SendCommand
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPortableDeviceService::SendCommand


## -description


The <b>SendCommand</b> method sends a standard WPD command and its parameters to the service.


## -parameters




### -param dwFlags [in]

Not used.


### -param pParameters [in]

The <a href="https://msdn.microsoft.com/a73cbb4e-15d2-4c8d-9267-aaec9a0fd09f">IPortableDeviceValues</a> interface specifying the command parameters.


### -param ppResults [out]

The <a href="https://msdn.microsoft.com/a73cbb4e-15d2-4c8d-9267-aaec9a0fd09f">IPortableDeviceValues</a> interface specifying the command results.


## -returns



If the method succeeds, it returns <b>S_OK</b>. Any other <b>HRESULT</b> value indicates that the call failed. 
          




## -remarks



This method should only be used to send standard WPD commands to the service. To invoke service methods, use the <a href="https://msdn.microsoft.com/9d233dea-91b6-4358-830c-6abe466264e5">IPortableDeviceServiceMethods</a> interface.

This method may fail even though it returns <b>S_OK</b> as its <b>HRESULT</b> value. To determine if a command succeeded, an application should always examine the properties referenced by the <i>ppResults</i> parameter:

<ul>
<li>The <a href="https://msdn.microsoft.com/en-us/library/Dd319305(v=VS.85).aspx">WPD_PROPERTY_COMMON_HRESULT</a> property indicates if the command succeeded.</li>
<li>If the command failed, the <a href="https://msdn.microsoft.com/en-us/library/Dd319305(v=VS.85).aspx">WPD_PROPERTY_COMMON_DRIVER_ERROR_CODE</a> property will contain driver-specific error codes.</li>
</ul>
The object referenced by the <i>pParameters</i> parameter must specify at least these properties:

<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/Dd319305(v=VS.85).aspx">WPD_PROPERTY_COMMON_COMMAND_CATEGORY</a>, which should contain a command category, such as the <b>fmtid</b> member of the <a href="https://msdn.microsoft.com/7a630cc9-02ea-46be-9645-8a0306606139">WPD_COMMAND_COMMON_RESET_DEVICE</a> property</li>
<li><a href="https://msdn.microsoft.com/en-us/library/Dd319305(v=VS.85).aspx">WPD_PROPERTY_COMMON_COMMAND_ID</a>, which should contain a command identifier, such as the <b>pid</b> member of the  <a href="https://msdn.microsoft.com/7a630cc9-02ea-46be-9645-8a0306606139">WPD_COMMAND_COMMON_RESET_DEVICE</a> property.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/f57344d5-c978-4c27-b8a9-b42492bd9312">IPortableDeviceService Interface</a>
 

 

