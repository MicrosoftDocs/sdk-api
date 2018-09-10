---
UID: NF:mdmregistration.GetDeviceRegistrationInfo
title: GetDeviceRegistrationInfo function
author: windows-sdk-content
description: Retrieves the device registration information.
old-location: mdmreg\getdeviceregistrationinfo.htm
tech.root: MDMReg
ms.assetid: 7FA2F81C-6714-42D8-880E-FD5A27A0F80A
ms.author: windowssdkdev
ms.date: 02/21/2018
ms.keywords: GetDeviceRegistrationInfo, GetDeviceRegistrationInfo function [MDM Registration], mdmreg.getdeviceregistrationinfo, mdmregistration/GetDeviceRegistrationInfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mdmregistration.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: MDMRegistration.lib
req.dll: MDMRegistration.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - MDMRegistration.dll
api_name:
 - GetDeviceRegistrationInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetDeviceRegistrationInfo function


## -description


Retrieves the device registration information.


## -parameters




### -param DeviceInformationClass [in]

Contains the maximum length that can be returned through the <i>pszHyperlink</i> 
      parameter.


### -param ppDeviceRegistrationInfo [out]

Details of the device registration.


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>. .




## -remarks



The caller of this function must be running as an elevated process.




## -see-also




<a href="https://msdn.microsoft.com/1f42ed5e-e221-47ec-a019-ed06c05d55d0">MDM Registration Error Values</a>



<a href="https://msdn.microsoft.com/1b063a56-f59f-4b02-949f-c8b6bbf45a13">MDM Registration Functions</a>
 

 

