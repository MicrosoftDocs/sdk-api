---
UID: NF:mdmregistration.GetDeviceRegistrationInfo
title: GetDeviceRegistrationInfo function (mdmregistration.h)
author: windows-sdk-content
description: Retrieves the device registration information.
old-location: mdmreg\getdeviceregistrationinfo.htm
tech.root: MDMReg
ms.assetid: 7FA2F81C-6714-42D8-880E-FD5A27A0F80A
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetDeviceRegistrationInfo, GetDeviceRegistrationInfo function [MDM Registration], mdmreg.getdeviceregistrationinfo, mdmregistration/GetDeviceRegistrationInfo
ms.topic: function
f1_keywords: 
 - "mdmregistration/GetDeviceRegistrationInfo"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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




<a href="https://docs.microsoft.com/windows/desktop/MDMReg/mdm-registration-constants">MDM Registration Error Values</a>



<a href="https://docs.microsoft.com/windows/desktop/MDMReg/mdm-registration-functions">MDM Registration Functions</a>
 

 

