---
UID: NC:stm.PIS_SERVICE
title: PIS_SERVICE (stm.h)
description: The IsService function checks whether a service of specified type and name exists in the service table, and optionally returns the service's parameters.
helpviewer_keywords: ["IsService","IsService callback function [RAS]","PIS_SERVICE","PIS_SERVICE callback","_mpr_isservice","rras.isservice","stm/IsService"]
old-location: rras\isservice.htm
tech.root: RRAS
ms.assetid: f2d8e1f4-ce6c-429c-bb14-26c6c75eab7e
ms.date: 12/05/2018
ms.keywords: IsService, IsService callback function [RAS], PIS_SERVICE, PIS_SERVICE callback, _mpr_isservice, rras.isservice, stm/IsService
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
 - PIS_SERVICE
 - stm/PIS_SERVICE
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
 - IsService
---

# PIS_SERVICE callback function


## -description

The 
<b>IsService</b> function checks whether a service of specified type and name exists in the service table, and optionally returns the service's parameters.

## -parameters

### -param Type [in]

Specifies the type of the service being checked.

### -param Name [in]

Specifies the name of the service being checked.

### -param Service [out]

Pointer to a structure in which to receive the information about the matching service (if any).

## -returns

The 
<b>IsService</b> function returns one of the following values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TRUE</b></dt>
</dl>
</td>
<td width="60%">
The service exists in the table.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
No such service exists, or the operation failed. Call 
<a href="/previous-versions/windows/desktop/wab/-wab-iabcontainer-getlasterror">GetLastError</a> for more information about the failure.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NO_ERROR</b></dt>
</dl>
</td>
<td width="60%">
The operation succeeded, but no such service exists.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The service type or name is invalid.

</td>
</tr>
</table>
 


<div> </div>

## -see-also

<a href="/previous-versions/windows/desktop/wab/-wab-iabcontainer-getlasterror">GetLastError</a>



<a href="/windows/desktop/RRAS/ipx-service-table-management">IPX Service Table Management</a>



<a href="/windows/desktop/api/stm/ns-stm-ipx_service">IPX_SERVICE</a>



<a href="/windows/desktop/RRAS/service-table-management-functions">Service Table Management Functions</a>