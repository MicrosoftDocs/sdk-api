---
UID: NF:vsprov.IVssSoftwareSnapshotProvider.BeginPrepareSnapshot
title: IVssSoftwareSnapshotProvider::BeginPrepareSnapshot (vsprov.h)
description: VSS calls this method for each shadow copy that is added to the shadow copy set. (IVssSoftwareSnapshotProvider.BeginPrepareSnapshot)
helpviewer_keywords: ["BeginPrepareSnapshot","BeginPrepareSnapshot method","BeginPrepareSnapshot method","IVssSoftwareSnapshotProvider interface","IVssSoftwareSnapshotProvider interface","BeginPrepareSnapshot method","IVssSoftwareSnapshotProvider.BeginPrepareSnapshot","IVssSoftwareSnapshotProvider::BeginPrepareSnapshot","base.ivsssoftwaresnapshotprovider_beginpreparesnapshot","vsprov/IVssSoftwareSnapshotProvider::BeginPrepareSnapshot"]
old-location: base\ivsssoftwaresnapshotprovider_beginpreparesnapshot.htm
tech.root: base
ms.assetid: 75e6a865-13e7-4bed-bd83-c74c4c1dc228
ms.date: 12/05/2018
ms.keywords: BeginPrepareSnapshot, BeginPrepareSnapshot method, BeginPrepareSnapshot method,IVssSoftwareSnapshotProvider interface, IVssSoftwareSnapshotProvider interface,BeginPrepareSnapshot method, IVssSoftwareSnapshotProvider.BeginPrepareSnapshot, IVssSoftwareSnapshotProvider::BeginPrepareSnapshot, base.ivsssoftwaresnapshotprovider_beginpreparesnapshot, vsprov/IVssSoftwareSnapshotProvider::BeginPrepareSnapshot
req.header: vsprov.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
req.lib: VssApi.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVssSoftwareSnapshotProvider::BeginPrepareSnapshot
 - vsprov/IVssSoftwareSnapshotProvider::BeginPrepareSnapshot
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - VssApi.lib
 - VssApi.dll
api_name:
 - IVssSoftwareSnapshotProvider.BeginPrepareSnapshot
---

# IVssSoftwareSnapshotProvider::BeginPrepareSnapshot


## -description

VSS calls this method for each shadow copy that is added to the shadow copy set.

## -parameters

### -param SnapshotSetId [in]

Shadow copy set identifier.

### -param SnapshotId [in]

Identifier of the shadow copy to be created.

### -param pwszVolumeName [in]

Null-terminated wide character string containing the volume name. The name must be in one of the following formats and must include a trailing backslash (\\): 




<ul>
<li>The path of a mounted folder, for example, Y:\MountX\</li>
<li>A drive letter, for example, D:\</li>
<li>A volume GUID path of the form \\?&#92;<i>Volume</i>{<i>GUID</i>}\ (where <i>GUID</i> identifies the volume)</li>
</ul>

### -param lNewContext [in]

The context for the shadow copy set. This context consists of a bitmask of <a href="/windows/desktop/api/vss/ne-vss-vss_volume_snapshot_attributes">_VSS_VOLUME_SNAPSHOT_ATTRIBUTES</a> values.

## -returns

The following are the valid return codes for this method.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The shadow copy was successfully created.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The caller does not have sufficient backup privileges or is not an administrator.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the parameter values is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The caller is out of memory or other system resources.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_OBJECT_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified volume was not found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_PROVIDER_VETO</b></dt>
</dl>
</td>
<td width="60%">
Provider error. The provider logged the error in the event log. For more information, see 
        <a href="/windows/desktop/VSS/event-and-error-handling-under-vss">Event and Error Handling Under VSS</a>.
       

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_UNSUPPORTED_CONTEXT</b></dt>
</dl>
</td>
<td width="60%">
The specified context is not supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_VOLUME_NOT_SUPPORTED_BY_PROVIDER</b></dt>
</dl>
</td>
<td width="60%">
The provider does not support the specified volume.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Unexpected error. The error code is logged in the error log file. For more information, see 
        <a href="/windows/desktop/VSS/event-and-error-handling-under-vss">Event and Error Handling Under VSS</a>.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not supported until Windows Server 2008 R2 and Windows 7. E_UNEXPECTED is used instead.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/vsprov/nn-vsprov-ivsssoftwaresnapshotprovider">IVssSoftwareSnapshotProvider</a>
