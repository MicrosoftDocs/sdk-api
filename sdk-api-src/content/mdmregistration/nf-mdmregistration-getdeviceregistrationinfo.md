---
UID: NF:mdmregistration.GetDeviceRegistrationInfo
title: GetDeviceRegistrationInfo function (mdmregistration.h)
description: Retrieves the device registration information.
helpviewer_keywords: ["GetDeviceRegistrationInfo","GetDeviceRegistrationInfo function [MDM Registration]","mdmreg.getdeviceregistrationinfo","mdmregistration/GetDeviceRegistrationInfo"]
old-location: mdmreg\getdeviceregistrationinfo.htm
tech.root: MDMReg
ms.assetid: 7FA2F81C-6714-42D8-880E-FD5A27A0F80A
ms.date: 12/05/2018
ms.keywords: GetDeviceRegistrationInfo, GetDeviceRegistrationInfo function [MDM Registration], mdmreg.getdeviceregistrationinfo, mdmregistration/GetDeviceRegistrationInfo
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetDeviceRegistrationInfo
 - mdmregistration/GetDeviceRegistrationInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - MDMRegistration.dll
api_name:
 - GetDeviceRegistrationInfo
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

<a href="/windows/desktop/MDMReg/mdm-registration-constants">MDM Registration Error Values</a>



<a href="/windows/desktop/MDMReg/mdm-registration-functions">MDM Registration Functions</a>