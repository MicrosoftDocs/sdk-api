---
UID: NC:stm.PCREATE_STATIC_SERVICE
title: PCREATE_STATIC_SERVICE (stm.h)
description: The CreateStaticService function adds a static service to the table.
helpviewer_keywords: ["CreateStaticService","CreateStaticService callback function [RAS]","PCREATE_STATIC_SERVICE","PCREATE_STATIC_SERVICE callback","_mpr_createstaticservice","rras.createstaticservice","stm/CreateStaticService"]
old-location: rras\createstaticservice.htm
tech.root: RRAS
ms.assetid: 529beae6-ba39-417c-8fa6-7b97fc720352
ms.date: 12/05/2018
ms.keywords: CreateStaticService, CreateStaticService callback function [RAS], PCREATE_STATIC_SERVICE, PCREATE_STATIC_SERVICE callback, _mpr_createstaticservice, rras.createstaticservice, stm/CreateStaticService
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
 - PCREATE_STATIC_SERVICE
 - stm/PCREATE_STATIC_SERVICE
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
 - CreateStaticService
---

# PCREATE_STATIC_SERVICE callback function


## -description

The 
<b>CreateStaticService</b> function adds a static service to the table.

## -parameters

### -param InterfaceIndex [in]

Specifies a unique number that identifies the interface associated with the new service.

### -param ServerEntry

#### - ServiceEntry [in]

Pointer to an 
<a href="/previous-versions/windows/desktop/legacy/aa374456(v=vs.85)">IPX_STATIC_SERVICE_INFO</a> structure that specifies parameters of the static service to be added.

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
One of the parameters is invalid.

</td>
</tr>
</table>
 


<div> </div>

## -see-also

<a href="/windows/desktop/api/stm/nc-stm-pdelete_static_service">DeleteStaticService</a>



<a href="/windows/desktop/RRAS/ipx-service-table-management">IPX Service Table Management</a>



<a href="/previous-versions/windows/desktop/legacy/aa374456(v=vs.85)">IPX_STATIC_SERVICE_INFO</a>



<a href="/windows/desktop/RRAS/service-table-management-functions">Service Table Management Functions</a>