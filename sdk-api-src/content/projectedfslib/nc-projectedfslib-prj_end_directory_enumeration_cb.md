---
UID: NC:projectedfslib.PRJ_END_DIRECTORY_ENUMERATION_CB
title: PRJ_END_DIRECTORY_ENUMERATION_CB (projectedfslib.h)
description: Informs the provider that a directory enumeration is over.
helpviewer_keywords: ["PRJ_END_DIRECTORY_ENUMERATION_CB","PRJ_END_DIRECTORY_ENUMERATION_CB callback","PRJ_END_DIRECTORY_ENUMERATION_CB callback function","ProjFS.prj_end_directory_enumeration_cb","projectedfslib/PRJ_END_DIRECTORY_ENUMERATION_CB"]
old-location: projfs\prj_end_directory_enumeration_cb.htm
tech.root: ProjFS
ms.assetid: E9DA86AC-E884-4DB3-977D-6D8EDA2A8E12
ms.date: 12/05/2018
ms.keywords: PRJ_END_DIRECTORY_ENUMERATION_CB, PRJ_END_DIRECTORY_ENUMERATION_CB callback, PRJ_END_DIRECTORY_ENUMERATION_CB callback function, ProjFS.prj_end_directory_enumeration_cb, projectedfslib/PRJ_END_DIRECTORY_ENUMERATION_CB
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
 - PRJ_END_DIRECTORY_ENUMERATION_CB
 - projectedfslib/PRJ_END_DIRECTORY_ENUMERATION_CB
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - ProjectedFSLib.h
api_name:
 - PRJ_END_DIRECTORY_ENUMERATION_CB
---

# PRJ_END_DIRECTORY_ENUMERATION_CB callback function


## -description

Informs the provider that a directory enumeration is over.

## -parameters

### -param callbackData [in]

Information about the operation. 


The provider can access this buffer only while the callback is running. If it wishes to pend the operation and it requires data from this buffer, it must make its own copy of it.

### -param enumerationId [in]

An identifier for this enumeration session. See the Remarks section of <a href="/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_start_directory_enumeration_cb">PRJ_START_DIRECTORY_ENUMERATION_CB</a> for more information.

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
The provider successfully completed the operation.

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
 

The provider should not return any other value from this callback.

## -remarks

For a user-initiated enumeration ProjFS invokes this callback when the file handle used to enumerate the directory is closed. For a ProjFS-initiated enumeration, this callback is invoked when ProjFS completes the enumeration.