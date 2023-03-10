---
UID: NC:scesvc.PFSCE_FREE_INFO
title: PFSCE_FREE_INFO (scesvc.h)
description: Frees the memory for buffers allocated by the Security Configuration tool set when it calls PFSCE_QUERY_INFO.
helpviewer_keywords: ["PFSCE_FREE_INFO","PFSCE_FREE_INFO callback","PFSCE_FREE_INFO callback function [Security]","_config_pfsce_free_info","scesvc/PFSCE_FREE_INFO","security.pfsce_free_info"]
old-location: security\pfsce_free_info.htm
tech.root: security
ms.assetid: e7cafdbc-9ca2-4bb1-b8ed-d5553acaf7bc
ms.date: 12/05/2018
ms.keywords: PFSCE_FREE_INFO, PFSCE_FREE_INFO callback, PFSCE_FREE_INFO callback function [Security], _config_pfsce_free_info, scesvc/PFSCE_FREE_INFO, security.pfsce_free_info
req.header: scesvc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - PFSCE_FREE_INFO
 - scesvc/PFSCE_FREE_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Scesvc.h
api_name:
 - PFSCE_FREE_INFO
---

# PFSCE_FREE_INFO callback function


## -description

The <a href="/windows/desktop/api/scesvc/nc-scesvc-pfsce_query_info">PFSCE_QUERY_INFO</a> callback function frees the memory for buffers allocated by the Security Configuration tool set when it calls 
<a href="/windows/desktop/api/scesvc/nc-scesvc-pfsce_query_info">PFSCE_QUERY_INFO</a>.

## -parameters

### -param pvServiceInfo [in]

Specifies a pointer to the buffer allocated by the Security Configuration tool set.

## -returns

If the function succeeds, it returns SCESTATUS_SUCCESS. Otherwise, an error code is returned. This can be the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SCESTATUS_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters passed into the function was not valid.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/scesvc/nc-scesvc-pfsce_query_info">PFSCE_QUERY_INFO</a>