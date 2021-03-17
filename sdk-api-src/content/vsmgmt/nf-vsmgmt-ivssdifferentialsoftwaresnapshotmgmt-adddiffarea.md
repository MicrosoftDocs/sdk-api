---
UID: NF:vsmgmt.IVssDifferentialSoftwareSnapshotMgmt.AddDiffArea
title: IVssDifferentialSoftwareSnapshotMgmt::AddDiffArea (vsmgmt.h)
description: Adds a shadow copy storage area association for the specified volume.
helpviewer_keywords: ["AddDiffArea","AddDiffArea method [VSS]","AddDiffArea method [VSS]","IVssDifferentialSoftwareSnapshotMgmt interface","IVssDifferentialSoftwareSnapshotMgmt interface [VSS]","AddDiffArea method","IVssDifferentialSoftwareSnapshotMgmt.AddDiffArea","IVssDifferentialSoftwareSnapshotMgmt::AddDiffArea","base.ivssdifferentialsoftwaresnapshotmgmt_adddiffarea","vsmgmt/IVssDifferentialSoftwareSnapshotMgmt::AddDiffArea"]
old-location: base\ivssdifferentialsoftwaresnapshotmgmt_adddiffarea.htm
tech.root: base
ms.assetid: 7b58331c-b8a2-4333-a05d-563395d5f0c2
ms.date: 12/05/2018
ms.keywords: AddDiffArea, AddDiffArea method [VSS], AddDiffArea method [VSS],IVssDifferentialSoftwareSnapshotMgmt interface, IVssDifferentialSoftwareSnapshotMgmt interface [VSS],AddDiffArea method, IVssDifferentialSoftwareSnapshotMgmt.AddDiffArea, IVssDifferentialSoftwareSnapshotMgmt::AddDiffArea, base.ivssdifferentialsoftwaresnapshotmgmt_adddiffarea, vsmgmt/IVssDifferentialSoftwareSnapshotMgmt::AddDiffArea
req.header: vsmgmt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
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
 - IVssDifferentialSoftwareSnapshotMgmt::AddDiffArea
 - vsmgmt/IVssDifferentialSoftwareSnapshotMgmt::AddDiffArea
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
 - IVssDifferentialSoftwareSnapshotMgmt.AddDiffArea
---

# IVssDifferentialSoftwareSnapshotMgmt::AddDiffArea


## -description

The <b>AddDiffArea</b> 
    method adds a shadow copy storage  area association for the specified volume. If the 
    association is not supported, an error code will be returned.

## -parameters

### -param pwszVolumeName [in]

The name of the volume that will be the source of shadow copies. This volume is associated with a shadow copy 
      storage area on the <i>pwszDiffAreaVolumeName</i> volume.
      

The name of the volume must be in one of the following formats and must include a trailing backslash (\\):
       <ul>
<li>The path of a mounted folder, for example, Y:\MountX\</li>
<li>A drive letter, for example, 
         D:\</li>
<li>A volume GUID path of the form \\?&#92;<i>Volume</i>{<i>GUID</i>}\ (where <i>GUID</i> identifies the volume)</li>
</ul>

### -param pwszDiffAreaVolumeName [in]

The name of the volume that will contain the  shadow copy storage  area to be associated with the 
      <i>pwszVolumeName</i> volume.
      

The name of the volume must be in one of the following formats and must include a trailing backslash (\\):
       <ul>
<li>The path of a mounted folder</li>
<li>A drive letter, for example, 
         D:\</li>
<li>A volume GUID path of the form \\?&#92;<i>Volume</i>{<i>GUID</i>}\ (where <i>GUID</i> identifies the volume)</li>
</ul>

### -param llMaximumDiffSpace [in]

The maximum size, in bytes, of the shadow copy storage area on the  volume. This value 
      must be at least 320 MB, up to the system-wide limit.
       If this value is –1, the maximum size is unlimited.

<b>Windows Server 2003:  </b>Prior to Windows Server 2003 with SP1, the shadow copy storage area size was fixed at 100 MB.

## -returns

This method can return one of these values.

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
Successfully added the shadow copy storage area association.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
Caller does not have sufficient backup privileges or is not an administrator.

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
<dt><b>VSS_E_MAXIMUM_DIFFAREA_ASSOCIATIONS_REACHED</b></dt>
</dl>
</td>
<td width="60%">
The maximum number of shadow copy storage areas has been added to the shadow copy source volume. The 
        specified shadow copy storage volume was not associated with the specified shadow copy source volume.

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
<dt><b>VSS_E_OBJECT_ALREADY_EXISTS</b></dt>
</dl>
</td>
<td width="60%">
The association between the <i>pwszVolumeName</i> and 
        <i>pwszDiffAreaVolumeName</i> volumes already exists.

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
<dt><b>VSS_E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Unexpected error. The error code is logged in the error log file. For more information, see 
        <a href="/windows/desktop/VSS/event-and-error-handling-under-vss">Event and Error Handling Under VSS</a>.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not supported until Windows Server 2008 R2 and Windows 7. E_UNEXPECTED is used instead.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_VOLUME_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The <i>pwszDiffAreaVolumeName</i> volume is not an NTFS volume or has insufficient free 
        space.

</td>
</tr>
</table>

## -remarks

A shadow copy storage area association cannot be created if any shadow copies already exist for the 
    <i>pwszVolumeName</i> volume or if there is already a shadow copy storage area association for 
    that volume.

The shadow copy storage area for a virtual hard disk (VHD) source volume must reside on the same volume. Likewise, a shadow copy storage area can only be created on a VHD volume if the source volume is the same for both volumes.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>VHDs are not supported.

To change the size of a shadow copy storage area, use the <a href="/windows/desktop/api/vsmgmt/nf-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt-changediffareamaximumsize">IVssDifferentialSoftwareSnapshotMgmt::ChangeDiffAreaMaximumSize</a> or <a href="/windows/desktop/api/vsmgmt/nf-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt2-changediffareamaximumsizeex">IVssDifferentialSoftwareSnapshotMgmt2::ChangeDiffAreaMaximumSizeEx</a> method. You can delete a shadow copy storage area by changing its size to zero.

## -see-also

<a href="/windows/desktop/api/vsmgmt/nn-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt">IVssDifferentialSoftwareSnapshotMgmt</a>