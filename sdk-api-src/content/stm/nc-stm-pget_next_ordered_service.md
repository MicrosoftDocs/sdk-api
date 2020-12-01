---
UID: NC:stm.PGET_NEXT_ORDERED_SERVICE
title: PGET_NEXT_ORDERED_SERVICE (stm.h)
description: The GetNextOrderedService function returns the next service from a subset of services in the table. The service returned is the next service after a given input service using the ordering method specified.
helpviewer_keywords: ["GetNextOrderedService","GetNextOrderedService callback function [RAS]","PGET_NEXT_ORDERED_SERVICE","PGET_NEXT_ORDERED_SERVICE callback","_mpr_getnextorderedservice","rras.getnextorderedservice","stm/GetNextOrderedService"]
old-location: rras\getnextorderedservice.htm
tech.root: RRAS
ms.assetid: e25d7086-cfb7-41ea-8f4e-7e4f065830d9
ms.date: 12/05/2018
ms.keywords: GetNextOrderedService, GetNextOrderedService callback function [RAS], PGET_NEXT_ORDERED_SERVICE, PGET_NEXT_ORDERED_SERVICE callback, _mpr_getnextorderedservice, rras.getnextorderedservice, stm/GetNextOrderedService
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PGET_NEXT_ORDERED_SERVICE
 - stm/PGET_NEXT_ORDERED_SERVICE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Stm.h
api_name:
 - GetNextOrderedService
---

# PGET_NEXT_ORDERED_SERVICE callback function


## -description

The 
<b>GetNextOrderedService</b> function returns the next service from a subset of services in the table. The service returned is the next service after a given input service using the ordering method specified.

## -parameters

### -param OrderingMethod [in]

Specifies the order in which the services are searched. See 
<a href="/windows/desktop/api/stm/nc-stm-pget_first_ordered_service">GetFirstOrderedService</a> for a description of the various ordering methods.

### -param ExclusionFlags [in]

Limits the set of examined services to a subset defined by <i>ExclusionFlags</i> and the values in the corresponding members of the structure pointed to by the <i>Service</i> parameter. See 
<a href="/windows/desktop/api/stm/nc-stm-pcreate_service_enumeration_handle">CreateServiceEnumerationHandle</a> for a description of the possible flags.

### -param Service [in, out]

Pointer to an 
<a href="/windows/desktop/api/stm/ns-stm-ipx_service">IPX_SERVICE</a> structure. 




On input, specifies the service from which to continue searching; also contains member values that correspond to the specified <i>ExclusionFlags</i>.

On output, the structure contains the first service that follows the input service and matches the specified criteria.

## -returns

If the function succeeds, the return value is NO_ERROR.

If the function fails, the return value is one of the following error codes.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_MORE_SERVICES</b></dt>
</dl>
</td>
<td width="60%">
There are no more services matching the specified criteria.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One of the  parameters is invalid.

</td>
</tr>
</table>
 


<div> </div>

## -see-also

<a href="/windows/desktop/api/stm/nc-stm-pcreate_service_enumeration_handle">CreateServiceEnumerationHandle</a>



<a href="/windows/desktop/RRAS/ipx-service-table-management">IPX Service Table Management</a>



<a href="/windows/desktop/api/stm/ns-stm-ipx_service">IPX_SERVICE</a>



<a href="/windows/desktop/RRAS/service-table-management-functions">Service Table Management Functions</a>