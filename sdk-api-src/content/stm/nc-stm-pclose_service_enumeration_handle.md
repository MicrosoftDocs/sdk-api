---
UID: NC:stm.PCLOSE_SERVICE_ENUMERATION_HANDLE
title: PCLOSE_SERVICE_ENUMERATION_HANDLE (stm.h)
description: The CloseServiceEnumerationHandle function terminates the enumeration and frees associated resources.helpviewer_keywords: ["CloseServiceEnumerationHandle","CloseServiceEnumerationHandle callback function [RAS]","PCLOSE_SERVICE_ENUMERATION_HANDLE","PCLOSE_SERVICE_ENUMERATION_HANDLE callback","_mpr_closeserviceenumerationhandle","rras.closeserviceenumerationhandle","stm/CloseServiceEnumerationHandle"]
old-location: rras\closeserviceenumerationhandle.htm
tech.root: RRAS
ms.assetid: c127f914-b655-4b6a-bb13-daeb5e82e343
ms.date: 12/05/2018
ms.keywords: CloseServiceEnumerationHandle, CloseServiceEnumerationHandle callback function [RAS], PCLOSE_SERVICE_ENUMERATION_HANDLE, PCLOSE_SERVICE_ENUMERATION_HANDLE callback, _mpr_closeserviceenumerationhandle, rras.closeserviceenumerationhandle, stm/CloseServiceEnumerationHandle
f1_keywords:
- stm/CloseServiceEnumerationHandle
dev_langs:
- c++
req.header: stm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- UserDefined
api_location:
- Stm.h
api_name:
- CloseServiceEnumerationHandle
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PCLOSE_SERVICE_ENUMERATION_HANDLE callback function


## -description


The 
<b>CloseServiceEnumerationHandle</b> function terminates the enumeration and frees associated resources.


## -parameters




### -param EnumerationHandle [in]

Handle that specifies the enumeration to terminate, obtained from a previous call to 
<a href="https://docs.microsoft.com/windows/desktop/api/stm/nc-stm-pcreate_service_enumeration_handle">CreateServiceEnumerationHandle</a>.


## -returns



If the functions succeeds, the return value is NO_ERROR.

If the function fails, the return value is ERROR_CAN_NOT_COMPLETE.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/stm/nc-stm-pcreate_service_enumeration_handle">CreateServiceEnumerationHandle</a>



<a href="https://docs.microsoft.com/windows/desktop/RRAS/ipx-service-table-management">IPX Service Table Management</a>



<a href="https://docs.microsoft.com/windows/desktop/RRAS/service-table-management-functions">Service Table Management Functions</a>
 

 

