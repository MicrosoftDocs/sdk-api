---
UID: NC:projectedfslib.PRJ_GET_DIRECTORY_ENUMERATION_CB
title: PRJ_GET_DIRECTORY_ENUMERATION_CB (projectedfslib.h)
description: Requests directory enumeration information from the provider.
helpviewer_keywords: ["PRJ_GET_DIRECTORY_ENUMERATION_CB","PRJ_GET_DIRECTORY_ENUMERATION_CB callback","PRJ_GET_DIRECTORY_ENUMERATION_CB callback function","ProjFS.prj_get_directory_enumeration_cb","projectedfslib/PRJ_GET_DIRECTORY_ENUMERATION_CB"]
old-location: projfs\prj_get_directory_enumeration_cb.htm
tech.root: ProjFS
ms.assetid: 45E7E7F9-9E54-44C8-9915-43CCECF85DB6
ms.date: 12/05/2018
ms.keywords: PRJ_GET_DIRECTORY_ENUMERATION_CB, PRJ_GET_DIRECTORY_ENUMERATION_CB callback, PRJ_GET_DIRECTORY_ENUMERATION_CB callback function, ProjFS.prj_get_directory_enumeration_cb, projectedfslib/PRJ_GET_DIRECTORY_ENUMERATION_CB
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
 - PRJ_GET_DIRECTORY_ENUMERATION_CB
 - projectedfslib/PRJ_GET_DIRECTORY_ENUMERATION_CB
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
 - PRJ_GET_DIRECTORY_ENUMERATION_CB
---

# PRJ_GET_DIRECTORY_ENUMERATION_CB callback function


## -description

Requests directory enumeration information from the provider.

## -parameters

### -param callbackData [in]

Information about the operation. The following <i>callbackData</i> members are necessary to implement this callback:<dl>
<dd><b>FilePathName</b> Identifies the directory to be enumerated.

</dd>
<dd><b>VersionInfo</b> Provides version information for the directory to be enumerated.

</dd>
<dd><b>Flags</b> Flags to control what is returned in the enumeration.  Valid values are:

<table>
<tr>
<td>PRJ_CB_DATA_FLAG_ENUM_RETURN_SINGLE_ENTRY</td>
<td>This bit is set if the user is requesting only one entry from the enumeration.  The provider may treat this as a hint, and may opt to return more than one entry to make an enumeration that returns one item at a time more efficient. 
In such a case ProjFS will return single entry to the user, invoking the provider only when it needs more entries.</td>
</tr>
<tr>
<td>PRJ_CB_DATA_FLAG_ENUM_RESTART_SCAN</td>
<td>This bit is set if the enumeration is to start at the first entry in the directory.  On the first invocation of this callback for an enumeration session the provider must treat this flag as set, regardless of its value. All enumerations must start at the first entry. 
On subsequent invocations of this callback the provider must honor this value.</td>
</tr>
</table>
 

</dd>
</dl>


The provider can access this buffer only while the callback is running. If it wishes to pend the operation and it requires data from this buffer, it must make its own copy of it.

### -param enumerationId [in]

An identifier for this enumeration session.

### -param searchExpression [in, optional]

A pointer to a null-terminated Unicode string specifying a search expression. The search expression may include wildcard characters. The provider should use the <a href="/windows/desktop/api/projectedfslib/nf-projectedfslib-prjdoesnamecontainwildcards">PrjDoesNameContainWildCards</a> function to determine whether wildcards are present in <b>searchExpression</b>, and it should use the <a href="/windows/desktop/api/projectedfslib/nf-projectedfslib-prjfilenamematch">PrjFileNameMatch</a> function to determine whether an entry in its backing store matches a search expression containing wildcards.

This parameter is optional and may be NULL.<ul>
<li>If this parameter is not NULL, the provider must return only those directory entries whose names match the search expression.</li>
<li>If this parameter is NULL, the provider must return all directory entries.</li>
</ul>


The provider should capture the value of this parameter on the first invocation of this callback for an enumeration session and use it on subsequent invocations, ignoring this parameter on those invocations unless <b>PRJ_CB_DATA_FLAG_ENUM_RESTART_SCAN</b> is specified in the <b>Flags</b> member of <b>callbackData</b>.  In that case the provider must re-capture the value of <b>searchExpression.</b>

### -param dirEntryBufferHandle [in]

An opaque handle to a structure that receives the results of the enumeration from the provider. The provider uses the <a href="/windows/desktop/api/projectedfslib/nf-projectedfslib-prjfilldirentrybuffer">PrjFillDirEntryBuffer</a> routine to fill the structure.

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
The provider successfully added at least one entry to dirEntryBufferHandle, or no entries in the provider’s store match searchExpression. 


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER)</b></dt>
</dl>
</td>
<td width="60%">
The provider received this error from <a href="/windows/desktop/api/projectedfslib/nf-projectedfslib-prjfilldirentrybuffer">PrjFillDirEntryBuffer</a> for the first file or directory it tried to add to dirEntryBufferHandle. 


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

ProjFS invokes this callback one or more times after invoking <a href="/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_start_directory_enumeration_cb">PRJ_START_DIRECTORY_ENUMERATION_CB</a>.  See the Remarks section of <i>PRJ_START_DIRECTORY_ENUMERATION_CB</i> for more information.