---
UID: NF:vsbackup.IsVolumeSnapshotted
title: IsVolumeSnapshotted function (vsbackup.h)
description: The IsVolumeSnapshotted function (vsbackup.h) determines whether any shadow copies exist for the specified volume.
helpviewer_keywords: ["IsVolumeSnapshotted","IsVolumeSnapshotted function [VSS]","IsVolumeSnapshottedInternal","_win32_isvolumesnapshotted","base.isvolumesnapshotted","vsbackup/IsVolumeSnapshotted","vsbackup/IsVolumeSnapshottedInternal"]
old-location: base\isvolumesnapshotted.htm
tech.root: base
ms.assetid: 308eddea-50e2-44c8-858f-315b8960a421
ms.date: 08/09/2022
ms.keywords: IsVolumeSnapshotted, IsVolumeSnapshotted function [VSS], IsVolumeSnapshottedInternal, _win32_isvolumesnapshotted, base.isvolumesnapshotted, vsbackup/IsVolumeSnapshotted, vsbackup/IsVolumeSnapshottedInternal
req.header: vsbackup.h
req.include-header: VsBackup.h, Vss.h, VsWriter.h
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
req.lib: VssApi.lib
req.dll: VssApi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IsVolumeSnapshotted
 - vsbackup/IsVolumeSnapshotted
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - VssApi.dll
 - Ext-MS-Win-Fs-VssAPI-L1-1-0.dll
api_name:
 - IsVolumeSnapshotted
 - IsVolumeSnapshottedInternal
---

# IsVolumeSnapshotted function


## -description

The <b>IsVolumeSnapshotted</b> function determines 
    whether any shadow copies exist for the specified volume.
<div class="alert"><b>Note</b>  This function is exported as <b>IsVolumeSnapshottedInternal</b>, but you should call <b>IsVolumeSnapshotted</b>, not <b>IsVolumeSnapshottedInternal</b>.</div><div> </div>

## -parameters

### -param pwszVolumeName [in]

Name of the volume. The name of the volume to be checked must be in one of the following formats and must include a trailing backslash (\\):

<ul>
<li>The path of a mounted folder, for example, Y:\MountX\</li>
<li>A drive letter, for example, 
        D:\</li>
<li>A volume GUID path of the form \\?&#92;<i>Volume</i>{<i>GUID</i>}\ (where <i>GUID</i> identifies the volume)</li>
</ul>

### -param pbSnapshotsPresent [out]

The value of this parameter is <b>TRUE</b> if the volume has a shadow copy, and 
      <b>FALSE</b> if the volume does not have a shadow copy.

### -param plSnapshotCapability [out]

A bit mask (or bitwise OR) of 
      <a href="/windows/desktop/api/vss/ne-vss-vss_snapshot_compatibility">VSS_SNAPSHOT_COMPATIBILITY</a> values that 
      indicates whether certain volume control or file I/O operations are disabled for the given volume if a shadow 
      copy of it exists.

## -returns

The return values listed here are in addition to the normal COM <b>HRESULT</b>s that may be returned at any time 
       from the function.

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
The function completed successfully.

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
One of the parameters is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Out of memory or other system resources.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_PROVIDER_VETO</b></dt>
</dl>
</td>
<td width="60%">
Expected provider error. The provider logged the error in the event log. For more information, see 
        <a href="/windows/desktop/VSS/event-and-error-handling-under-vss">Event and Error Handling Under VSS</a>.

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
<dt><b>VSS_E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Unexpected error. The error code is logged in the error log file. For more information, see 
        <a href="/windows/desktop/VSS/event-and-error-handling-under-vss">Event and Error Handling Under VSS</a>.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not supported until Windows Server 2008 R2 and Windows 7. <b>E_UNEXPECTED</b> is used instead.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_UNEXPECTED_PROVIDER_ERROR</b></dt>
</dl>
</td>
<td width="60%">
Unexpected provider error. The error code is logged in the event log file. For additional information, 
        see 
        <a href="/windows/desktop/VSS/event-and-error-handling-under-vss">Event and Error Handling Under VSS</a>.

</td>
</tr>
</table>

## -remarks

Before calling this function, the caller must have initialized COM by calling the <a href="/windows/desktop/api/objbase/nf-objbase-coinitialize">CoInitialize</a> function.

If no volume control or file I/O operations are disabled for the selected volume, then the shadow copy 
    capability of the selected volume returned by <i>plSnapshotCapability</i> will be zero.

## -see-also

<a href="/windows/desktop/api/vss/ne-vss-vss_snapshot_compatibility">VSS_SNAPSHOT_COMPATIBILITY</a>
