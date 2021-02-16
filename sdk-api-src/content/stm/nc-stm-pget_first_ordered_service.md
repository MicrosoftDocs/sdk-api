---
UID: NC:stm.PGET_FIRST_ORDERED_SERVICE
title: PGET_FIRST_ORDERED_SERVICE (stm.h)
description: The GetFirstOrderedService function returns the first service in the specified order from the designated subset of services in the table.
helpviewer_keywords: ["GetFirstOrderedService","GetFirstOrderedService callback function [RAS]","PGET_FIRST_ORDERED_SERVICE","PGET_FIRST_ORDERED_SERVICE callback","STM_ORDER_BY_INTERFACE_TYPE_NAME","STM_ORDER_BY_TYPE_AND_NAME","_mpr_getfirstorderedservice","rras.getfirstorderedservice","stm/GetFirstOrderedService"]
old-location: rras\getfirstorderedservice.htm
tech.root: RRAS
ms.assetid: 193ca671-3b1a-493f-a655-a27f6348f5d2
ms.date: 12/05/2018
ms.keywords: GetFirstOrderedService, GetFirstOrderedService callback function [RAS], PGET_FIRST_ORDERED_SERVICE, PGET_FIRST_ORDERED_SERVICE callback, STM_ORDER_BY_INTERFACE_TYPE_NAME, STM_ORDER_BY_TYPE_AND_NAME, _mpr_getfirstorderedservice, rras.getfirstorderedservice, stm/GetFirstOrderedService
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
 - PGET_FIRST_ORDERED_SERVICE
 - stm/PGET_FIRST_ORDERED_SERVICE
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
 - GetFirstOrderedService
---

# PGET_FIRST_ORDERED_SERVICE callback function


## -description

The 
<b>GetFirstOrderedService</b> function returns the first service in the specified order from the designated subset of services in the table.

## -parameters

### -param OrderingMethod [in]

Specifies the order in which the services are searched. This parameter must be one of the following values. 


					

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="STM_ORDER_BY_TYPE_AND_NAME"></a><a id="stm_order_by_type_and_name"></a><dl>
<dt><b>STM_ORDER_BY_TYPE_AND_NAME</b></dt>
</dl>
</td>
<td width="60%">
Search the services first by type and then by name.

</td>
</tr>
<tr>
<td width="40%"><a id="STM_ORDER_BY_INTERFACE_TYPE_NAME"></a><a id="stm_order_by_interface_type_name"></a><dl>
<dt><b>STM_ORDER_BY_INTERFACE_TYPE_NAME</b></dt>
</dl>
</td>
<td width="60%">
Search the services first by interface index, then by type, and finally by name.

</td>
</tr>
</table>

### -param ExclusionFlags [in]

Specifies the limits the set of examined services to a subset defined by <i>ExclusionFlags</i> and the values in the members of the structure pointed to by the <i>Service</i> parameter. See 
<a href="/windows/desktop/api/stm/nc-stm-pcreate_service_enumeration_handle">CreateServiceEnumerationHandle</a> for a description of the possible flags.

### -param Service [in, out]

Pointer to an 
<a href="/windows/desktop/api/stm/ns-stm-ipx_service">IPX_SERVICE</a> structure. 




On input, the values in the members correspond to flags specified in <i>ExclusionFlags</i>.

On output, the first service that matches specified criteria.

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
<dt><b>ERROR_NO_MORE_ITEMS</b></dt>
</dl>
</td>
<td width="60%">
Services that match the specified criteria do not exist.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters is invalid.

</td>
</tr>
</table>
 


<div> </div>

## -see-also

<a href="/windows/desktop/api/stm/nc-stm-pcreate_service_enumeration_handle">CreateServiceEnumerationHandle</a>



<a href="/windows/desktop/RRAS/ipx-service-table-management">IPX Service Table Management</a>



<a href="/windows/desktop/api/stm/ns-stm-ipx_service">IPX_SERVICE</a>



<a href="/windows/desktop/RRAS/service-table-management-functions">Service Table Management Functions</a>