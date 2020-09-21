---
UID: NF:mdmregistration.RegisterDeviceWithManagementUsingAADCredentials
title: RegisterDeviceWithManagementUsingAADCredentials function (mdmregistration.h)
description: Registers a device with a MDM service, using Azure Active Directory (AAD) credentials.
helpviewer_keywords: ["RegisterDeviceWithManagementUsingAADCredentials","RegisterDeviceWithManagementUsingAADCredentials function [MDM Registration]","mdmreg.registerdevicewithmanagementusingaadcredentials","mdmregistration/RegisterDeviceWithManagementUsingAADCredentials"]
old-location: mdmreg\registerdevicewithmanagementusingaadcredentials.htm
tech.root: MDMReg
ms.assetid: 709E464A-C9EC-41EF-AC80-EF0BC35E0905
ms.date: 12/05/2018
ms.keywords: RegisterDeviceWithManagementUsingAADCredentials, RegisterDeviceWithManagementUsingAADCredentials function [MDM Registration], mdmreg.registerdevicewithmanagementusingaadcredentials, mdmregistration/RegisterDeviceWithManagementUsingAADCredentials
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
 - RegisterDeviceWithManagementUsingAADCredentials
 - mdmregistration/RegisterDeviceWithManagementUsingAADCredentials
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
 - RegisterDeviceWithManagementUsingAADCredentials
---

# RegisterDeviceWithManagementUsingAADCredentials function


## -description

Registers a device with a MDM service, using Azure Active Directory (AAD) credentials.

## -parameters

### -param UserToken [in]

The User to impersonate when attempting to get AAD token

## -returns

If the function succeeds, the return value is <b>ERROR_SUCCESS</b>. If the function fails, the returned value describes the error. Possible 
      values include those listed at 
      <a href="/windows/desktop/MDMReg/mdm-registration-constants">MDM Registration Error Values</a>.

## -remarks

The caller of this function must be running as an elevated process.

## -see-also

<a href="/windows/desktop/MDMReg/mdm-registration-constants">MDM Registration Error Values</a>



<a href="/windows/desktop/MDMReg/mdm-registration-functions">MDM Registration Functions</a>



<a href="/windows/desktop/api/mdmregistration/nf-mdmregistration-unregisterdevicewithmanagement">UnregisterDeviceWithManagement</a>