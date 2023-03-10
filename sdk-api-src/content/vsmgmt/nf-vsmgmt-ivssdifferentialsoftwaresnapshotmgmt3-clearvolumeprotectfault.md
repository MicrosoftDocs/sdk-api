---
UID: NF:vsmgmt.IVssDifferentialSoftwareSnapshotMgmt3.ClearVolumeProtectFault
title: IVssDifferentialSoftwareSnapshotMgmt3::ClearVolumeProtectFault (vsmgmt.h)
description: Clears the protection fault state for the specified volume.
helpviewer_keywords: ["ClearVolumeProtectFault","ClearVolumeProtectFault method","ClearVolumeProtectFault method","IVssDifferentialSoftwareSnapshotMgmt3 interface","IVssDifferentialSoftwareSnapshotMgmt3 interface","ClearVolumeProtectFault method","IVssDifferentialSoftwareSnapshotMgmt3.ClearVolumeProtectFault","IVssDifferentialSoftwareSnapshotMgmt3::ClearVolumeProtectFault","base.ivssdifferentialsoftwaresnapshotmgmt3_clearvolumeprotectfault","vsmgmt/IVssDifferentialSoftwareSnapshotMgmt3::ClearVolumeProtectFault"]
old-location: base\ivssdifferentialsoftwaresnapshotmgmt3_clearvolumeprotectfault.htm
tech.root: base
ms.assetid: 07257d34-23b1-47bf-b613-f65f5d2a977e
ms.date: 12/05/2018
ms.keywords: ClearVolumeProtectFault, ClearVolumeProtectFault method, ClearVolumeProtectFault method,IVssDifferentialSoftwareSnapshotMgmt3 interface, IVssDifferentialSoftwareSnapshotMgmt3 interface,ClearVolumeProtectFault method, IVssDifferentialSoftwareSnapshotMgmt3.ClearVolumeProtectFault, IVssDifferentialSoftwareSnapshotMgmt3::ClearVolumeProtectFault, base.ivssdifferentialsoftwaresnapshotmgmt3_clearvolumeprotectfault, vsmgmt/IVssDifferentialSoftwareSnapshotMgmt3::ClearVolumeProtectFault
req.header: vsmgmt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - IVssDifferentialSoftwareSnapshotMgmt3::ClearVolumeProtectFault
 - vsmgmt/IVssDifferentialSoftwareSnapshotMgmt3::ClearVolumeProtectFault
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - VsMgmt.h
api_name:
 - IVssDifferentialSoftwareSnapshotMgmt3.ClearVolumeProtectFault
---

# IVssDifferentialSoftwareSnapshotMgmt3::ClearVolumeProtectFault


## -description

Clears the protection fault state for the specified volume.

## -parameters

### -param pwszVolumeName [in]

The name of the volume.
      This parameter is required and cannot be <b>NULL</b>.

The name must be in one of the following formats and must include a trailing backslash (\\):
       <ul>
<li>The path of a mounted folder, for example, Y:\MountX\</li>
<li>A drive letter, for example, D:\ 
         </li>
<li>A volume GUID path in the form \\?&#92;<i>Volume</i>{<i>GUID</i>}\ (where <i>GUID</i> identifies the volume)</li>
</ul>

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
The protection fault state was cleared successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
<dt>0x80070005L</dt>
</dl>
</td>
<td width="60%">
The caller is not an administrator.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
<dt>0x80070057L</dt>
</dl>
</td>
<td width="60%">
One of the parameter values is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
<dt>0x80000001L</dt>
</dl>
</td>
<td width="60%">
The provider for the volume does not support shadow copy protection.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_PROVIDER_VETO</b></dt>
<dt>0x80042306L</dt>
</dl>
</td>
<td width="60%">
An expected provider error has occurred. The error code is logged in the event log. For more information, see <a href="/windows/desktop/VSS/event-and-error-handling-under-vss">Event and Error Handling Under VSS</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_OBJECT_NOT_FOUND</b></dt>
<dt>0x80042308L</dt>
</dl>
</td>
<td width="60%">
The specified volume was not found.

</td>
</tr>
</table>

## -remarks

The <b>ClearVolumeProtectFault</b> method dismounts the volume and resets the volume's protection fault member to <b>FALSE</b> to allow normal I/O to continue on the volume. If the volume is not in a faulted state, this method does nothing.

## -see-also

<a href="/windows/desktop/api/vsmgmt/nn-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt3">IVssDifferentialSoftwareSnapshotMgmt3</a>