---
UID: NC:stm.PBLOCK_DELETE_STATIC_SERVICES
title: PBLOCK_DELETE_STATIC_SERVICES (stm.h)
description: The BlockDeleteStaticServices function deletes all static services associated with a specified interface.
helpviewer_keywords: ["BlockDeleteStaticServices","BlockDeleteStaticServices callback function [RAS]","PBLOCK_DELETE_STATIC_SERVICES","PBLOCK_DELETE_STATIC_SERVICES callback","_mpr_blockdeletestaticservices","rras.blockdeletestaticservices","stm/BlockDeleteStaticServices"]
old-location: rras\blockdeletestaticservices.htm
tech.root: RRAS
ms.assetid: eb680a9c-aad8-44b5-8c20-af15c1fd8930
ms.date: 12/05/2018
ms.keywords: BlockDeleteStaticServices, BlockDeleteStaticServices callback function [RAS], PBLOCK_DELETE_STATIC_SERVICES, PBLOCK_DELETE_STATIC_SERVICES callback, _mpr_blockdeletestaticservices, rras.blockdeletestaticservices, stm/BlockDeleteStaticServices
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
 - PBLOCK_DELETE_STATIC_SERVICES
 - stm/PBLOCK_DELETE_STATIC_SERVICES
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
 - BlockDeleteStaticServices
---

# PBLOCK_DELETE_STATIC_SERVICES callback function


## -description

The 
<b>BlockDeleteStaticServices</b> function deletes all static services associated with a specified interface.

## -parameters

### -param InterfaceIndex [in]

Specifies the unique number that identifies the interface associated with the services to be deleted.

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

<a href="/windows/desktop/api/stm/nc-stm-pblock_convert_services_to_static">BlockConvertServicesToStatic</a>



<a href="/windows/desktop/RRAS/ipx-service-table-management">IPX Service Table Management</a>



<a href="/windows/desktop/RRAS/service-table-management-functions">Service Table Management Functions</a>