---
UID: NF:mdmregistration.IsDeviceRegisteredWithManagement
title: IsDeviceRegisteredWithManagement function (mdmregistration.h)
description: Checks whether the device is registered with an MDM service.
helpviewer_keywords: ["IsDeviceRegisteredWithManagement","IsDeviceRegisteredWithManagement function [MDM Registration]","mdmreg.isdeviceregisteredwithmanagement","mdmregistration/IsDeviceRegisteredWithManagement"]
old-location: mdmreg\isdeviceregisteredwithmanagement.htm
tech.root: MDMReg
ms.assetid: 7f8b4965-0acd-4e64-8756-37e7bf96ab6e
ms.date: 12/05/2018
ms.keywords: IsDeviceRegisteredWithManagement, IsDeviceRegisteredWithManagement function [MDM Registration], mdmreg.isdeviceregisteredwithmanagement, mdmregistration/IsDeviceRegisteredWithManagement
req.header: mdmregistration.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1
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
 - IsDeviceRegisteredWithManagement
 - mdmregistration/IsDeviceRegisteredWithManagement
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - MDMRegistration.dll
 - MDMRegistration2.dll
api_name:
 - IsDeviceRegisteredWithManagement
---

# IsDeviceRegisteredWithManagement function


## -description

Checks whether the device is registered with an MDM service. If the device is registered, 
    it also returns the user principal name (UPN) of the registered user.

## -parameters

### -param pfIsDeviceRegisteredWithManagement [out]

Address of a <b>BOOL</b> indicates whether the device is registered.

### -param cchUPN [in, optional]

Contains the maximum length that can be returned through the <i>pszUPN</i> 
      parameter.

### -param pszUPN [out, optional]

Optional address of a buffer that receives the  <b>NULL</b>-terminated Unicode string 
      containing the UPN of the user registered with the management service. If <i>pszUPN</i> is 
      <b>NULL</b> then the <b>BOOL</b> pointed to by the 
      <i>pfIsDeviceRegisteredWithManagement</i> parameter is updated to indicate whether the device 
      is registered and the function returns <b>ERROR_SUCCESS</b>.

## -returns

If the function succeeds, the return value is <b>ERROR_SUCCESS</b> and the 
       <b>BOOL</b> pointed to by the 
       <i>pfIsDeviceRegisteredWithManagement</i> parameter contains <b>TRUE</b> 
       or <b>FALSE</b>. If <b>TRUE</b>, the Unicode string pointed to by the 
       <i>pszUPN</i> parameter contains the UPN of the registered user. If the function fails, the 
       returned value describes the error. Possible values include those listed at 
       <a href="/windows/desktop/MDMReg/mdm-registration-constants">MDM Registration Error Values</a>.

If the buffer size indicated by the <i>cchUPN</i> parameter is too small then the call will fail with 
       <b>STRSAFE_E_INSUFFICIENT_BUFFER</b> but the <b>BOOL</b> pointed to by 
       the <i>pfIsDeviceRegisteredWithManagement</i> parameter will be updated to indicate whether 
       the device is registered.

## -see-also

<a href="/windows/desktop/MDMReg/mdm-registration-constants">MDM Registration Error Values</a>



<a href="/windows/desktop/MDMReg/mdm-registration-functions">MDM Registration Functions</a>