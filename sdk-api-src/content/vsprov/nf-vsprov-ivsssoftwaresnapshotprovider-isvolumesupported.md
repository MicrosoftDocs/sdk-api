---
UID: NF:vsprov.IVssSoftwareSnapshotProvider.IsVolumeSupported
title: IVssSoftwareSnapshotProvider::IsVolumeSupported (vsprov.h)
description: Determines whether the provider supports shadow copies on the specified volume.
helpviewer_keywords: ["IVssSoftwareSnapshotProvider interface","IsVolumeSupported method","IVssSoftwareSnapshotProvider.IsVolumeSupported","IVssSoftwareSnapshotProvider::IsVolumeSupported","IsVolumeSupported","IsVolumeSupported method","IsVolumeSupported method","IVssSoftwareSnapshotProvider interface","base.ivsssoftwaresnapshotprovider_isvolumesupported","vsprov/IVssSoftwareSnapshotProvider::IsVolumeSupported"]
old-location: base\ivsssoftwaresnapshotprovider_isvolumesupported.htm
tech.root: base
ms.assetid: 5dbaa5ad-4a35-49e2-a528-de1ea38e6e0b
ms.date: 12/05/2018
ms.keywords: IVssSoftwareSnapshotProvider interface,IsVolumeSupported method, IVssSoftwareSnapshotProvider.IsVolumeSupported, IVssSoftwareSnapshotProvider::IsVolumeSupported, IsVolumeSupported, IsVolumeSupported method, IsVolumeSupported method,IVssSoftwareSnapshotProvider interface, base.ivsssoftwaresnapshotprovider_isvolumesupported, vsprov/IVssSoftwareSnapshotProvider::IsVolumeSupported
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
 - IVssSoftwareSnapshotProvider::IsVolumeSupported
 - vsprov/IVssSoftwareSnapshotProvider::IsVolumeSupported
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
 - IVssSoftwareSnapshotProvider.IsVolumeSupported
---

# IVssSoftwareSnapshotProvider::IsVolumeSupported


## -description

Determines whether the provider supports shadow copies on the specified volume.

## -parameters

### -param pwszVolumeName [in]

Null-terminated wide character string containing the volume name. The name must be in one of the following formats and must include a trailing backslash (\\): 




<ul>
<li>The path of a mounted folder, for example, Y:\MountX\</li>
<li>A drive letter, for example, D:\</li>
<li>A volume GUID path of the form \\?&#92;<i>Volume</i>{<i>GUID</i>}\ (where <i>GUID</i> identifies the volume)</li>
</ul>

### -param pbSupportedByThisProvider [out]

This parameter receives <b>TRUE</b> if shadow copies are supported on the specified volume, otherwise <b>FALSE</b>.

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
<dt><b>VSS_E_NESTED_VOLUME_LIMIT</b></dt>
</dl>
</td>
<td width="60%">
The specified volume is nested too deeply to participate in the VSS operation.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This return code is not supported.

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

The <b>IsVolumeSupported</b> method will return <b>TRUE</b> if it is possible to create shadow copies on the given volume, even if the current configuration does not allow the creation of shadow copies on that volume at the present time.

For example, if the maximum number of shadow copies has been reached on a given volume (and therefore no more shadow copies can be created on that volume), the method will still indicate that the volume can be shadow copied.

This method cannot be called for a virtual hard disk (VHD) that is nested inside another VHD.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>VHDs are not supported.

## -see-also

<a href="/windows/desktop/api/vsprov/nn-vsprov-ivsssoftwaresnapshotprovider">IVssSoftwareSnapshotProvider</a>