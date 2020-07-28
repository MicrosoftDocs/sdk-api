---
UID: NC:stm.PENUMERATE_GET_NEXT_SERVICE
title: PENUMERATE_GET_NEXT_SERVICE (stm.h)
description: The EnumerateGetNextService function returns the next service entry in an enumeration started by CreateServiceEnumerationHandle.
helpviewer_keywords: ["EnumerateGetNextService","EnumerateGetNextService callback function [RAS]","PENUMERATE_GET_NEXT_SERVICE","PENUMERATE_GET_NEXT_SERVICE callback","_mpr_enumerategetnextservice","rras.enumerategetnextservice","stm/EnumerateGetNextService"]
old-location: rras\enumerategetnextservice.htm
tech.root: RRAS
ms.assetid: 45d0ccaa-97d5-4a14-9983-dc0ca268ed4b
ms.date: 12/05/2018
ms.keywords: EnumerateGetNextService, EnumerateGetNextService callback function [RAS], PENUMERATE_GET_NEXT_SERVICE, PENUMERATE_GET_NEXT_SERVICE callback, _mpr_enumerategetnextservice, rras.enumerategetnextservice, stm/EnumerateGetNextService
f1_keywords:
- stm/EnumerateGetNextService
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
- EnumerateGetNextService
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PENUMERATE_GET_NEXT_SERVICE callback function


## -description


The 
<b>EnumerateGetNextService</b> function returns the next service entry in an enumeration started by 
<a href="https://docs.microsoft.com/windows/desktop/api/stm/nc-stm-pcreate_service_enumeration_handle">CreateServiceEnumerationHandle</a>.


## -parameters




### -param EnumerationHandle [in]

Handle that identifies the enumeration and specifies the subset of services on which the enumeration will operate. The handle is obtained from a call to 
<a href="https://docs.microsoft.com/windows/desktop/api/stm/nc-stm-pcreate_service_enumeration_handle">CreateServiceEnumerationHandle</a>.


### -param Service [out]

Pointer to an 
<a href="https://docs.microsoft.com/windows/desktop/api/stm/ns-stm-ipx_service">IPX_SERVICE</a> structure that contains the next service in the enumeration. The services are returned in no particular order, and each service in the subset is returned only once.


## -returns



If the function succeeds, the buffer pointed to by the <i>Service</i> parameter receives the next service in the enumeration. In this case the return value is NO_ERROR.

If the function fails, the return value is one of the following error codes.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_MORE_ITEMS</b></dt>
</dl>
</td>
<td width="60%">
No more services exist with the specified criteria.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_CAN_NOT_COMPLETE</b></dt>
</dl>
</td>
<td width="60%">
The operation failed.

</td>
</tr>
</table>
 


<div> </div>





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/stm/nc-stm-pcreate_service_enumeration_handle">CreateServiceEnumerationHandle</a>



<a href="https://docs.microsoft.com/windows/desktop/RRAS/ipx-service-table-management">IPX Service Table Management</a>



<a href="https://docs.microsoft.com/windows/desktop/api/stm/ns-stm-ipx_service">IPX_SERVICE</a>



<a href="https://docs.microsoft.com/windows/desktop/RRAS/service-table-management-functions">Service Table Management Functions</a>
 

 

