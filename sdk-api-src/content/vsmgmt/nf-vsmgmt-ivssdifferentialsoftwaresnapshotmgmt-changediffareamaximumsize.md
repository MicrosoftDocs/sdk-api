---
UID: NF:vsmgmt.IVssDifferentialSoftwareSnapshotMgmt.ChangeDiffAreaMaximumSize
title: IVssDifferentialSoftwareSnapshotMgmt::ChangeDiffAreaMaximumSize (vsmgmt.h)
description: Updates the shadow copy storage area maximum size for a certain volume.
helpviewer_keywords: ["ChangeDiffAreaMaximumSize","ChangeDiffAreaMaximumSize method [VSS]","ChangeDiffAreaMaximumSize method [VSS]","IVssDifferentialSoftwareSnapshotMgmt interface","IVssDifferentialSoftwareSnapshotMgmt interface [VSS]","ChangeDiffAreaMaximumSize method","IVssDifferentialSoftwareSnapshotMgmt.ChangeDiffAreaMaximumSize","IVssDifferentialSoftwareSnapshotMgmt::ChangeDiffAreaMaximumSize","base.ivssdifferentialsoftwaresnapshotmgmt_changediffareamaximumsize","vsmgmt/IVssDifferentialSoftwareSnapshotMgmt::ChangeDiffAreaMaximumSize"]
old-location: base\ivssdifferentialsoftwaresnapshotmgmt_changediffareamaximumsize.htm
tech.root: base
ms.assetid: c7773fa8-6b43-46bf-b644-0016b261c080
ms.date: 12/05/2018
ms.keywords: ChangeDiffAreaMaximumSize, ChangeDiffAreaMaximumSize method [VSS], ChangeDiffAreaMaximumSize method [VSS],IVssDifferentialSoftwareSnapshotMgmt interface, IVssDifferentialSoftwareSnapshotMgmt interface [VSS],ChangeDiffAreaMaximumSize method, IVssDifferentialSoftwareSnapshotMgmt.ChangeDiffAreaMaximumSize, IVssDifferentialSoftwareSnapshotMgmt::ChangeDiffAreaMaximumSize, base.ivssdifferentialsoftwaresnapshotmgmt_changediffareamaximumsize, vsmgmt/IVssDifferentialSoftwareSnapshotMgmt::ChangeDiffAreaMaximumSize
req.header: vsmgmt.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVssDifferentialSoftwareSnapshotMgmt::ChangeDiffAreaMaximumSize
 - vsmgmt/IVssDifferentialSoftwareSnapshotMgmt::ChangeDiffAreaMaximumSize
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
 - IVssDifferentialSoftwareSnapshotMgmt.ChangeDiffAreaMaximumSize
---

# IVssDifferentialSoftwareSnapshotMgmt::ChangeDiffAreaMaximumSize


## -description

The 
    <b>ChangeDiffAreaMaximumSize</b> 
    method updates the shadow copy storage area maximum size for a certain volume. This may not 
    have an immediate effect.

## -parameters

### -param pwszVolumeName [in]

Name of the volume that is the source of shadow copies. This volume is associated with a shadow copy storage area 
      on the <i>pwszDiffAreaVolumeName</i> volume.
      

The name of the volume must be in one of the following formats and must include a trailing backslash (\\):
       <ul>
<li>The path of a mounted folder, for example, Y:\MountX\</li>
<li>A drive letter, for example, 
         D:\</li>
<li>A volume GUID path of the form \\?&#92;<i>Volume</i>{<i>GUID</i>}\ (where <i>GUID</i> identifies the volume)</li>
</ul>

### -param pwszDiffAreaVolumeName [in]

Name of the volume that contains the  shadow copy storage  area associated with the 
      <i>pwszVolumeName</i> volume.
      

The name of the volume must be in one of the following formats and must include a trailing backslash (\\):
       <ul>
<li>The path of a mounted folder</li>
<li>A drive letter, for example, 
         D:\</li>
<li>A volume GUID path of the form \\?&#92;<i>Volume</i>{<i>GUID</i>}\ (where <i>GUID</i> identifies the volume)</li>
</ul>

### -param llMaximumDiffSpace [in]

Specifies the maximum size, in bytes, for the shadow copy storage area to use for the volume. If this value is zero, 
      the shadow copy storage area will be deleted. If this value is –1, the maximum size is unlimited.

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
Successfully changed the shadow copy storage area maximum size.

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
<dt><b>VSS_E_INSUFFICIENT_STORAGE</b></dt>
</dl>
</td>
<td width="60%">
The <i>pwszDiffAreaVolumeName</i> volume does not have sufficient free space.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_OBJECT_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The association between the <i>pwszVolumeName</i> and 
        <i>pwszDiffAreaVolumeName</i> volumes was not found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_PROVIDER_VETO</b></dt>
</dl>
</td>
<td width="60%">
Provider error - the provider logged the error in the event log. For more information, see 
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
<dt><b>VSS_E_VOLUME_IN_USE</b></dt>
</dl>
</td>
<td width="60%">
A shadow copy is currently using the shadow copy storage area.

</td>
</tr>
</table>

## -remarks

The <b>ChangeDiffAreaMaximumSize</b> method makes the shadow copy storage area explicit, which means that it is not deleted automatically when all shadow copies are deleted.

If the shadow copy storage area does not exist, this method creates it.

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b>If the shadow copy storage area does not exist, this method does not create it.

To create a shadow copy storage area, use the <a href="/windows/desktop/api/vsmgmt/nf-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt-adddiffarea">IVssDifferentialSoftwareSnapshotMgmt::AddDiffArea</a> method.

## -see-also

<a href="/windows/desktop/api/vsmgmt/nn-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt">IVssDifferentialSoftwareSnapshotMgmt</a>