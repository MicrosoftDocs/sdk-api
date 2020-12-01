---
UID: NC:stm.PBLOCK_CONVERT_SERVICES_TO_STATIC
title: PBLOCK_CONVERT_SERVICES_TO_STATIC (stm.h)
description: The BlockConvertServicesToStatic function converts all services received on a specified interface to static.
helpviewer_keywords: ["BlockConvertServicesToStatic","BlockConvertServicesToStatic callback function [RAS]","PBLOCK_CONVERT_SERVICES_TO_STATIC","PBLOCK_CONVERT_SERVICES_TO_STATIC callback","_mpr_blockconvertservicestostatic","rras.blockconvertservicestostatic","stm/BlockConvertServicesToStatic"]
old-location: rras\blockconvertservicestostatic.htm
tech.root: RRAS
ms.assetid: 60d1ee7b-bba3-4dd1-8faf-520a2e3cfad3
ms.date: 12/05/2018
ms.keywords: BlockConvertServicesToStatic, BlockConvertServicesToStatic callback function [RAS], PBLOCK_CONVERT_SERVICES_TO_STATIC, PBLOCK_CONVERT_SERVICES_TO_STATIC callback, _mpr_blockconvertservicestostatic, rras.blockconvertservicestostatic, stm/BlockConvertServicesToStatic
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
 - PBLOCK_CONVERT_SERVICES_TO_STATIC
 - stm/PBLOCK_CONVERT_SERVICES_TO_STATIC
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
 - BlockConvertServicesToStatic
---

# PBLOCK_CONVERT_SERVICES_TO_STATIC callback function


## -description

The 
<b>BlockConvertServicesToStatic</b> function converts all services received on a specified interface to static.

## -parameters

### -param InterfaceIndex [in]

Specifies the unique number that identifies the interface associated with the services intended for conversion.

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
<dt><b>ERROR_CAN_NOT_COMPLETE</b></dt>
</dl>
</td>
<td width="60%">
The SAP Agent is down.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The parameter is invalid.

</td>
</tr>
</table>
 


<div> </div>

## -see-also

<a href="/windows/desktop/api/stm/nc-stm-pblock_delete_static_services">BlockDeleteStaticServices</a>



<a href="/windows/desktop/RRAS/ipx-service-table-management">IPX Service Table Management</a>



<a href="/windows/desktop/RRAS/service-table-management-functions">Service Table Management Functions</a>