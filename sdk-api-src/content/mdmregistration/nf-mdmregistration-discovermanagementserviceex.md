---
UID: NF:mdmregistration.DiscoverManagementServiceEx
title: DiscoverManagementServiceEx function (mdmregistration.h)
description: Discovers the MDM service using a candidate server.
helpviewer_keywords: ["DiscoverManagementServiceEx","DiscoverManagementServiceEx function [MDM Registration]","mdmreg.discovermanagementserviceex","mdmregistration/DiscoverManagementServiceEx"]
old-location: mdmreg\discovermanagementserviceex.htm
tech.root: MDMReg
ms.assetid: 600269ff-df88-49ed-b151-df0302cbc4d4
ms.date: 12/05/2018
ms.keywords: DiscoverManagementServiceEx, DiscoverManagementServiceEx function [MDM Registration], mdmreg.discovermanagementserviceex, mdmregistration/DiscoverManagementServiceEx
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
 - DiscoverManagementServiceEx
 - mdmregistration/DiscoverManagementServiceEx
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
 - DiscoverManagementServiceEx
---

# DiscoverManagementServiceEx function


## -description

Discovers the MDM service using a candidate server. The discovery process uses the 
    <a href="/openspecs/windows_protocols/ms-mde/5c841535-042e-489e-913c-9d783d741267">[MS-MDE]: Mobile Device Enrollment Protocol</a> 
    protocol.

## -parameters

### -param pszUPN [in]

Address of a <b>NULL</b>-terminated Unicode string containing the user principal name 
      (UPN) of the user requesting registration.

### -param pszDiscoveryServiceCandidate [in]

Address of a <b>NULL</b>-terminated Unicode string containing the discovery service 
      candidate to use in lieu of automatic discovery.

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

This function is not available before Windows Server 2012 R2 Update and Windows 8.1 Update.

## -see-also

<a href="/windows/desktop/api/mdmregistration/nf-mdmregistration-discovermanagementservice">DiscoverManagementService</a>



<a href="/windows/win32/api/mdmregistration/ns-mdmregistration-management_service_info">MANAGEMENT_SERVICE_INFO</a>



<a href="/windows/desktop/MDMReg/mdm-registration-constants">MDM Registration Error Values</a>



<a href="/windows/desktop/MDMReg/mdm-registration-functions">MDM Registration Functions</a>