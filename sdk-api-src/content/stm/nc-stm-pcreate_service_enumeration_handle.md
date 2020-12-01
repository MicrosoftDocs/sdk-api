---
UID: NC:stm.PCREATE_SERVICE_ENUMERATION_HANDLE
title: PCREATE_SERVICE_ENUMERATION_HANDLE (stm.h)
description: The CreateServiceEnumerationHandle function returns a handle that allows the use of fast and change-tolerant enumeration functions.
helpviewer_keywords: ["CreateServiceEnumerationHandle","CreateServiceEnumerationHandle callback function [RAS]","PCREATE_SERVICE_ENUMERATION_HANDLE","PCREATE_SERVICE_ENUMERATION_HANDLE callback","STM_ONLY_THIS_INTERFACE","STM_ONLY_THIS_PROTOCOL","STM_ONLY_THIS_TYPE","_mpr_createserviceenumerationhandle","rras.createserviceenumerationhandle","stm/CreateServiceEnumerationHandle"]
old-location: rras\createserviceenumerationhandle.htm
tech.root: RRAS
ms.assetid: 68ed5662-ffa8-456b-b79c-a6fb27339262
ms.date: 12/05/2018
ms.keywords: CreateServiceEnumerationHandle, CreateServiceEnumerationHandle callback function [RAS], PCREATE_SERVICE_ENUMERATION_HANDLE, PCREATE_SERVICE_ENUMERATION_HANDLE callback, STM_ONLY_THIS_INTERFACE, STM_ONLY_THIS_PROTOCOL, STM_ONLY_THIS_TYPE, _mpr_createserviceenumerationhandle, rras.createserviceenumerationhandle, stm/CreateServiceEnumerationHandle
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
 - PCREATE_SERVICE_ENUMERATION_HANDLE
 - stm/PCREATE_SERVICE_ENUMERATION_HANDLE
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
 - CreateServiceEnumerationHandle
---

# PCREATE_SERVICE_ENUMERATION_HANDLE callback function


## -description

The 
<b>CreateServiceEnumerationHandle</b> function returns a handle that allows the use of fast and change-tolerant enumeration functions. Such functions can scan through all services or a specified subset. The functions are change-tolerant in that they automatically enumerate any changes that other processes make to the set of enumerated services

## -parameters

### -param ExclusionFlags [in]

Specifies the limits the set of services that 
<b>CreateServiceEnumerationHandle</b> returns to a subset defined by a combination of <i>ExclusionFlags</i> and values in the corresponding members of <i>CriteriaService</i>. This parameter is one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="STM_ONLY_THIS_INTERFACE"></a><a id="stm_only_this_interface"></a><dl>
<dt><b>STM_ONLY_THIS_INTERFACE</b></dt>
</dl>
</td>
<td width="60%">
Enumerate only those services that were obtained through the interface specified in the <b>InterfaceIndex</b> member of <i>CriteriaService</i>.

</td>
</tr>
<tr>
<td width="40%"><a id="STM_ONLY_THIS_PROTOCOL"></a><a id="stm_only_this_protocol"></a><dl>
<dt><b>STM_ONLY_THIS_PROTOCOL</b></dt>
</dl>
</td>
<td width="60%">
Enumerate only those services that were obtained through the protocol specified in the <b>Protocol</b> member of <i>CriteriaService</i>. For example, IPX_PROTOCOL_SAP for services obtained by the DLL protocol or IPX_PROTOCOL_STATIC for services maintained by the router manager.

</td>
</tr>
<tr>
<td width="40%"><a id="STM_ONLY_THIS_TYPE"></a><a id="stm_only_this_type"></a><dl>
<dt><b>STM_ONLY_THIS_TYPE</b></dt>
</dl>
</td>
<td width="60%">
Enumerate only those services that have the same type as those in the <b>Service</b> member of <i>CriteriaService</i>

</td>
</tr>
</table>

### -param CriteriaService [in]

Pointer to an 
<a href="/windows/desktop/api/stm/ns-stm-ipx_service">IPX_SERVICE</a> structure with member values that correspond to those specified in <i>ExclusionFlags</i>.

## -returns

If the function succeeds, the return value is a handle for use with the service enumeration function.

A <b>NULL</b> handle indicates no services exists with the specified criteria, or that the operation failed. For more information, call 
<a href="/previous-versions/windows/desktop/wab/-wab-iabcontainer-getlasterror">GetLastError</a> and check the error code against the table below.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_SERVICES</b></dt>
</dl>
</td>
<td width="60%">
No services exist with the specified criteria.

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

<a href="/windows/desktop/api/stm/nc-stm-pclose_service_enumeration_handle">CloseServiceEnumerationHandle</a>



<a href="/windows/desktop/api/stm/nc-stm-penumerate_get_next_service">EnumerateGetNextService</a>



<a href="/previous-versions/windows/desktop/wab/-wab-iabcontainer-getlasterror">GetLastError</a>



<a href="/windows/desktop/RRAS/ipx-service-table-management">IPX Service Table Management</a>



<a href="/windows/desktop/api/stm/ns-stm-ipx_service">IPX_SERVICE</a>



<a href="/windows/desktop/RRAS/service-table-management-functions">Service Table Management Functions</a>