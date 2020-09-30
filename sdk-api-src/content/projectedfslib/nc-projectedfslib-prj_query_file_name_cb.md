---
UID: NC:projectedfslib.PRJ_QUERY_FILE_NAME_CB
title: PRJ_QUERY_FILE_NAME_CB (projectedfslib.h)
description: Determines whether a given file path exists in the provider's backing store.
helpviewer_keywords: ["PRJ_QUERY_FILE_NAME_CB","PRJ_QUERY_FILE_NAME_CB callback","PRJ_QUERY_FILE_NAME_CB callback function","ProjFS.prj_query_file_name_cb","projectedfslib/PRJ_QUERY_FILE_NAME_CB"]
old-location: projfs\prj_query_file_name_cb.htm
tech.root: ProjFS
ms.assetid: 1B218D41-AF24-48C2-9E11-7E0455CE15AC
ms.date: 12/05/2018
ms.keywords: PRJ_QUERY_FILE_NAME_CB, PRJ_QUERY_FILE_NAME_CB callback, PRJ_QUERY_FILE_NAME_CB callback function, ProjFS.prj_query_file_name_cb, projectedfslib/PRJ_QUERY_FILE_NAME_CB
req.header: projectedfslib.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1809 [desktop apps only]
req.target-min-winversvr: Windows Server [desktop apps only]
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
ms.custom: RS5, 19H1
f1_keywords:
 - PRJ_QUERY_FILE_NAME_CB
 - projectedfslib/PRJ_QUERY_FILE_NAME_CB
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - projectedfslib.h
api_name:
 - PRJ_QUERY_FILE_NAME_CB
---

# PRJ_QUERY_FILE_NAME_CB callback function


## -description

Determines whether a given file path exists in the provider's backing store.

## -parameters

### -param callbackData [in]

Information about the operation.

## -returns

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The queried file path exists in the provider's store.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_FILE_NOT_FOUND)</b></dt>
</dl>
</td>
<td width="60%">
The queried file path does not exist in the provider's store.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_IO_PENDING)</b></dt>
</dl>
</td>
<td width="60%">
The provider wishes to complete the operation at a later time. 


</td>
</tr>
</table>
 

An appropriate HRESULT error code if the provider fails the operation.

## -remarks

This callback is optional.  If the provider does not supply an implementation of this callback, ProjFS will invoke the provider’s directory enumeration callbacks to determine the existence of a file path in the provider's store.

The provider should use <a href="/windows/desktop/api/projectedfslib/nf-projectedfslib-prjfilenamecompare">PrjFileNameCompare</a> as the comparison routine when searching its backing store for the specified file.