---
UID: NF:portabledeviceapi.IPortableDeviceService.SendCommand
title: IPortableDeviceService::SendCommand method
author: windows-driver-content
description: Sends a standard WPD command and its parameters to the service.
old-location: wpdsdk\iportabledeviceservice_sendcommand.htm
old-project: wpd_sdk
ms.assetid: c6c42347-145c-4be7-bea6-34b13c211cb1
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IPortableDeviceService, IPortableDeviceService interface [Windows Portable Devices SDK], SendCommand method, IPortableDeviceService::SendCommand, SendCommand method [Windows Portable Devices SDK], SendCommand method [Windows Portable Devices SDK], IPortableDeviceService interface, SendCommand,IPortableDeviceService.SendCommand, portabledeviceapi/IPortableDeviceService::SendCommand, wpdsdk.iportabledeviceservice_sendcommand
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: portabledeviceapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps | UWP apps]
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
req.typenames: WPD_WHITE_BALANCE_SETTINGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	PortableDeviceAPI.h
api_name:
-	IPortableDeviceService.SendCommand
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IPortableDeviceService::SendCommand method


## -description


The <b>SendCommand</b> method sends a standard WPD command and its parameters to the service.


## -parameters




### -param dwFlags [in]

Not used.


### -param pParameters [in]

The <a href="https://msdn.microsoft.com/library/windows/hardware/ff597597">IPortableDeviceValues</a> interface specifying the command parameters.


### -param ppResults [out]

The <a href="https://msdn.microsoft.com/library/windows/hardware/ff597597">IPortableDeviceValues</a> interface specifying the command results.


## -returns



If the method succeeds, it returns <b>S_OK</b>. Any other <b>HRESULT</b> value indicates that the call failed. 
          




## -remarks



This method should only be used to send standard WPD commands to the service. To invoke service methods, use the <a href="https://msdn.microsoft.com/9d233dea-91b6-4358-830c-6abe466264e5">IPortableDeviceServiceMethods</a> interface.

This method may fail even though it returns <b>S_OK</b> as its <b>HRESULT</b> value. To determine if a command succeeded, an application should always examine the properties referenced by the <i>ppResults</i> parameter:

<ul>
<li>The <a href="common_properties.htm">WPD_PROPERTY_COMMON_HRESULT</a> property indicates if the command succeeded.</li>
<li>If the command failed, the <a href="common_properties.htm">WPD_PROPERTY_COMMON_DRIVER_ERROR_CODE</a> property will contain driver-specific error codes.</li>
</ul>
The object referenced by the <i>pParameters</i> parameter must specify at least these properties:

<ul>
<li><a href="common_properties.htm">WPD_PROPERTY_COMMON_COMMAND_CATEGORY</a>, which should contain a command category, such as the <b>fmtid</b> member of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff597754">WPD_COMMAND_COMMON_RESET_DEVICE</a> property</li>
<li><a href="common_properties.htm">WPD_PROPERTY_COMMON_COMMAND_ID</a>, which should contain a command identifier, such as the <b>pid</b> member of the  <a href="https://msdn.microsoft.com/library/windows/hardware/ff597754">WPD_COMMAND_COMMON_RESET_DEVICE</a> property.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/f57344d5-c978-4c27-b8a9-b42492bd9312">IPortableDeviceService Interface</a>
 

 

