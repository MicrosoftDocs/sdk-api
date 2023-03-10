---
UID: NF:vsprov.IVssSoftwareSnapshotProvider.IsVolumeSnapshotted
title: IVssSoftwareSnapshotProvider::IsVolumeSnapshotted (vsprov.h)
description: Determines whether any shadow copies exist for the specified volume.
helpviewer_keywords: ["IVssSoftwareSnapshotProvider interface","IsVolumeSnapshotted method","IVssSoftwareSnapshotProvider.IsVolumeSnapshotted","IVssSoftwareSnapshotProvider::IsVolumeSnapshotted","IsVolumeSnapshotted","IsVolumeSnapshotted method","IsVolumeSnapshotted method","IVssSoftwareSnapshotProvider interface","base.ivsssoftwaresnapshotprovider_isvolumesnapshotted","vsprov/IVssSoftwareSnapshotProvider::IsVolumeSnapshotted"]
old-location: base\ivsssoftwaresnapshotprovider_isvolumesnapshotted.htm
tech.root: base
ms.assetid: 0dd8cbe4-a8f8-479c-b8f7-ccdd255e978a
ms.date: 12/05/2018
ms.keywords: IVssSoftwareSnapshotProvider interface,IsVolumeSnapshotted method, IVssSoftwareSnapshotProvider.IsVolumeSnapshotted, IVssSoftwareSnapshotProvider::IsVolumeSnapshotted, IsVolumeSnapshotted, IsVolumeSnapshotted method, IsVolumeSnapshotted method,IVssSoftwareSnapshotProvider interface, base.ivsssoftwaresnapshotprovider_isvolumesnapshotted, vsprov/IVssSoftwareSnapshotProvider::IsVolumeSnapshotted
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
 - IVssSoftwareSnapshotProvider::IsVolumeSnapshotted
 - vsprov/IVssSoftwareSnapshotProvider::IsVolumeSnapshotted
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
 - IVssSoftwareSnapshotProvider.IsVolumeSnapshotted
---

# IVssSoftwareSnapshotProvider::IsVolumeSnapshotted


## -description

Determines whether any shadow copies exist for the specified volume.

## -parameters

### -param pwszVolumeName [in]

Null-terminated wide character string containing the volume name. The name must be in one of the following formats and must include a trailing backslash (\\): 




<ul>
<li>The path of a mounted folder, for example, Y:\MountX\</li>
<li>A drive letter, for example, D:\</li>
<li>A volume GUID path of the form \\?&#92;<i>Volume</i>{<i>GUID</i>}\ (where GUID identifies the volume)</li>
</ul>

### -param pbSnapshotsPresent [out]

This parameter receives <b>TRUE</b> if the volume has a shadow copy, or <b>FALSE</b> if the volume does not have a shadow copy.

### -param plSnapshotCompatibility [out]

A bitmask of <a href="/windows/desktop/api/vss/ne-vss-vss_snapshot_compatibility">VSS_SNAPSHOT_COMPATIBILITY</a> values that indicate whether certain volume control or file I/O operations are disabled for the given volume, if the volume has a shadow copy.

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
The requested information was successfully returned.

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

## -remarks

If no volume control or file I/O operations are disabled for the selected volume, then the shadow copy capability of the selected volume returned by <i>plSnapshotCapability</i> will be zero.

## -see-also

<a href="/windows/desktop/api/vsprov/nn-vsprov-ivsssoftwaresnapshotprovider">IVssSoftwareSnapshotProvider</a>