---
UID: NF:mdmregistration.RegisterDeviceWithManagement
title: RegisterDeviceWithManagement function (mdmregistration.h)
description: Registers a device with a MDM service, using the [MS-MDE]:\_Mobile Device Enrollment Protocol.
helpviewer_keywords: ["RegisterDeviceWithManagement","RegisterDeviceWithManagement function [MDM Registration]","mdmreg.registerdevicewithmanagement","mdmregistration/RegisterDeviceWithManagement"]
old-location: mdmreg\registerdevicewithmanagement.htm
tech.root: MDMReg
ms.assetid: 3a927d98-decf-464a-82db-561e9abcfe29
ms.date: 12/05/2018
ms.keywords: RegisterDeviceWithManagement, RegisterDeviceWithManagement function [MDM Registration], mdmreg.registerdevicewithmanagement, mdmregistration/RegisterDeviceWithManagement
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
 - RegisterDeviceWithManagement
 - mdmregistration/RegisterDeviceWithManagement
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
 - RegisterDeviceWithManagement
---

# RegisterDeviceWithManagement function


## -description

Registers a device with a MDM service, using the 
    <a href="/openspecs/windows_protocols/ms-mde/5c841535-042e-489e-913c-9d783d741267">[MS-MDE]: Mobile Device Enrollment Protocol</a>.

## -parameters

### -param pszUPN [in]

Address of a <b>NULL</b>-terminated Unicode string containing the user principal name 
      (UPN) of the user requesting the registration.

<b>Windows 8.1:  </b>This parameter was located after the <i>ppszMDMServiceUri</i> parameter in Windows 8.1.

### -param ppszMDMServiceUri [in]

Address of a <b>NULL</b>-terminated Unicode string containing the URI of the MDM 
      service.

### -param ppzsAccessToken [in]

Address of a <b>NULL</b>-terminated Unicode string containing a token acquired from 
      a Secure Token Service which the management service will use to validate the user.

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