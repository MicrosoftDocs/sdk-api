---
UID: NF:mdmregistration.IsManagementRegistrationAllowed
title: IsManagementRegistrationAllowed function (mdmregistration.h)
description: Checks whether MDM registration is allowed by local policy.
helpviewer_keywords: ["IsManagementRegistrationAllowed","IsManagementRegistrationAllowed function [MDM Registration]","mdmreg.ismanagementregistrationallowed","mdmregistration/IsManagementRegistrationAllowed"]
old-location: mdmreg\ismanagementregistrationallowed.htm
tech.root: MDMReg
ms.assetid: 138f567d-4c50-4e13-be10-269eb44f9fe5
ms.date: 12/05/2018
ms.keywords: IsManagementRegistrationAllowed, IsManagementRegistrationAllowed function [MDM Registration], mdmreg.ismanagementregistrationallowed, mdmregistration/IsManagementRegistrationAllowed
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
 - IsManagementRegistrationAllowed
 - mdmregistration/IsManagementRegistrationAllowed
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
 - IsManagementRegistrationAllowed
---

# IsManagementRegistrationAllowed function


## -description

Checks whether MDM registration is allowed by local policy.

## -parameters

### -param pfIsManagementRegistrationAllowed [out]

Address of a <b>BOOL</b> that receives a value indication whether registration is allowed.

## -returns

If the function succeeds, the return value is <b>ERROR_SUCCESS</b> and the <b>BOOL</b> pointed to by the <i>pfIsManagementRegistrationAllowed</i> parameter contains <b>TRUE</b> or <b>FALSE</b>. If the function fails, the returned value describes the error. Possible 
      values include those listed at 
      <a href="/windows/desktop/MDMReg/mdm-registration-constants">MDM Registration Error Values</a>.

## -remarks

The caller of this function must be running as an elevated process.

## -see-also

<a href="/windows/desktop/MDMReg/mdm-registration-constants">MDM Registration Error Values</a>



<a href="/windows/desktop/MDMReg/mdm-registration-functions">MDM Registration Functions</a>



<a href="/windows/desktop/api/mdmregistration/nf-mdmregistration-setmanagedexternally">SetManagedExternally</a>