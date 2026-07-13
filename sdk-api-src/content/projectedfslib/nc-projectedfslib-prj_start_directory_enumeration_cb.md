---
UID: NC:projectedfslib.PRJ_START_DIRECTORY_ENUMERATION_CB
title: PRJ_START_DIRECTORY_ENUMERATION_CB (projectedfslib.h)
description: Informs the provider that a directory enumeration is starting.
helpviewer_keywords: ["PRJ_START_DIRECTORY_ENUMERATION_CB","PRJ_START_DIRECTORY_ENUMERATION_CB callback","PRJ_START_DIRECTORY_ENUMERATION_CB callback function","ProjFS.prj_start_directory_enumeration_cb","projectedfslib/PRJ_START_DIRECTORY_ENUMERATION_CB"]
old-location: projfs\prj_start_directory_enumeration_cb.htm
tech.root: ProjFS
ms.assetid: 09F284D4-BF39-42C9-A89B-DDC8201362EE
ms.date: 12/05/2018
ms.keywords: PRJ_START_DIRECTORY_ENUMERATION_CB, PRJ_START_DIRECTORY_ENUMERATION_CB callback, PRJ_START_DIRECTORY_ENUMERATION_CB callback function, ProjFS.prj_start_directory_enumeration_cb, projectedfslib/PRJ_START_DIRECTORY_ENUMERATION_CB
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
 - PRJ_START_DIRECTORY_ENUMERATION_CB
 - projectedfslib/PRJ_START_DIRECTORY_ENUMERATION_CB
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
 - PRJ_START_DIRECTORY_ENUMERATION_CB
---

# PRJ_START_DIRECTORY_ENUMERATION_CB callback function


## -description

Informs the provider that a directory enumeration is starting.

## -parameters

### -param callbackData [in]

Information about the operation. The following <i>callbackData</i> members are necessary to implement this callback:<dl>
<dd><b>FilePathName</b> Identifies the directory to be enumerated.

</dd>
<dd><b>VersionInfo</b> Provides version information for the directory to be enumerated.

</dd>
</dl>


The provider can access this buffer only while the callback is running. If it wishes to pend the operation and it requires data from this buffer, it must make its own copy of it.

### -param enumerationId [in]

An identifier for this enumeration session.

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
<dt><b>HRESULT_FROM_WIN32(ERROR_FILE_NOT_FOUND)</b></dt>
</dl>
</td>
<td width="60%">
The directory to be enumerated does not exist in the provider’s backing store. 


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

ProjFS requests a directory enumeration from the provider by first invoking this callback, then one or more <a href="/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_get_directory_enumeration_cb">PRJ_GET_DIRECTORY_ENUMERATION_CB</a> callbacks, then the <a href="/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_end_directory_enumeration_cb">PRJ_END_DIRECTORY_ENUMERATION_CB</a> callback. Because multiple enumerations may occur in parallel in the same location, ProjFS uses the <i>enumerationId</i> argument to associate the callback invocations into a single enumeration session, meaning that a given set of calls to the enumeration callbacks will use the same value for <i>enumerationId</i> for the same session.