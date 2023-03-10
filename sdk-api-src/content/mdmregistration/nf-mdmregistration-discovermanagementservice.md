---
UID: NF:mdmregistration.DiscoverManagementService
title: DiscoverManagementService function (mdmregistration.h)
description: Discovers the MDM service.
helpviewer_keywords: ["DiscoverManagementService","DiscoverManagementService function [MDM Registration]","mdmreg.discovermanagementservice","mdmregistration/DiscoverManagementService"]
old-location: mdmreg\discovermanagementservice.htm
tech.root: MDMReg
ms.assetid: 0b01225c-83db-4b13-ad7e-52beae05a8ee
ms.date: 12/05/2018
ms.keywords: DiscoverManagementService, DiscoverManagementService function [MDM Registration], mdmreg.discovermanagementservice, mdmregistration/DiscoverManagementService
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
 - DiscoverManagementService
 - mdmregistration/DiscoverManagementService
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
 - DiscoverManagementService
---

# DiscoverManagementService function


## -description

Discovers the MDM service. The discovery process uses the 
    <a href="/openspecs/windows_protocols/ms-mde/5c841535-042e-489e-913c-9d783d741267">[MS-MDE]: Mobile Device Enrollment Protocol</a> 
    protocol.

## -parameters

### -param pszUPN [in]

Address of a <b>NULL</b>-terminated Unicode string containing the user principal name 
      (UPN) of the user requesting registration.

### -param ppMgmtInfo [out]

Address of a <a href="/windows/win32/api/mdmregistration/ns-mdmregistration-management_service_info">MANAGEMENT_SERVICE_INFO</a> 
      structure that contains pointers to the URIs of the management and authentication services.

## -returns

If the function succeeds, the return value is <b>ERROR_SUCCESS</b>. If the function 
      fails, the returned value describes the error. Possible 
      values include those listed at 
      <a href="/windows/desktop/MDMReg/mdm-registration-constants">MDM Registration Error Values</a>.

## -remarks

The caller of this function must be running as an elevated process.

## -see-also

<a href="/windows/win32/api/mdmregistration/ns-mdmregistration-management_service_info">MANAGEMENT_SERVICE_INFO</a>



<a href="/windows/desktop/MDMReg/mdm-registration-constants">MDM Registration Error Values</a>



<a href="/windows/desktop/MDMReg/mdm-registration-functions">MDM Registration Functions</a>