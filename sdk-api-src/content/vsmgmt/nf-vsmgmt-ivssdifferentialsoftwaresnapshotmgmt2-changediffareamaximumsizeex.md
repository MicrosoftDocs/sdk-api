---
UID: NF:vsmgmt.IVssDifferentialSoftwareSnapshotMgmt2.ChangeDiffAreaMaximumSizeEx
title: IVssDifferentialSoftwareSnapshotMgmt2::ChangeDiffAreaMaximumSizeEx (vsmgmt.h)
description: Updates the shadow copy storage area maximum size for a certain volume. This may not have an immediate effect. If the bVolatile parameter is FALSE, the change continues even if the computer is rebooted.
helpviewer_keywords: ["ChangeDiffAreaMaximumSizeEx","ChangeDiffAreaMaximumSizeEx method","ChangeDiffAreaMaximumSizeEx method","IVssDifferentialSoftwareSnapshotMgmt2 interface","IVssDifferentialSoftwareSnapshotMgmt2 interface","ChangeDiffAreaMaximumSizeEx method","IVssDifferentialSoftwareSnapshotMgmt2.ChangeDiffAreaMaximumSizeEx","IVssDifferentialSoftwareSnapshotMgmt2::ChangeDiffAreaMaximumSizeEx","base.ivssdifferentialsoftwaresnapshotmgmt2_changediffareamaximumsizeex","vsmgmt/IVssDifferentialSoftwareSnapshotMgmt2::ChangeDiffAreaMaximumSizeEx"]
old-location: base\ivssdifferentialsoftwaresnapshotmgmt2_changediffareamaximumsizeex.htm
tech.root: base
ms.assetid: 9ba621d5-32ec-4512-a18f-dbdadbd3ff09
ms.date: 12/05/2018
ms.keywords: ChangeDiffAreaMaximumSizeEx, ChangeDiffAreaMaximumSizeEx method, ChangeDiffAreaMaximumSizeEx method,IVssDifferentialSoftwareSnapshotMgmt2 interface, IVssDifferentialSoftwareSnapshotMgmt2 interface,ChangeDiffAreaMaximumSizeEx method, IVssDifferentialSoftwareSnapshotMgmt2.ChangeDiffAreaMaximumSizeEx, IVssDifferentialSoftwareSnapshotMgmt2::ChangeDiffAreaMaximumSizeEx, base.ivssdifferentialsoftwaresnapshotmgmt2_changediffareamaximumsizeex, vsmgmt/IVssDifferentialSoftwareSnapshotMgmt2::ChangeDiffAreaMaximumSizeEx
req.header: vsmgmt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
 - IVssDifferentialSoftwareSnapshotMgmt2::ChangeDiffAreaMaximumSizeEx
 - vsmgmt/IVssDifferentialSoftwareSnapshotMgmt2::ChangeDiffAreaMaximumSizeEx
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
 - IVssDifferentialSoftwareSnapshotMgmt2.ChangeDiffAreaMaximumSizeEx
---

# IVssDifferentialSoftwareSnapshotMgmt2::ChangeDiffAreaMaximumSizeEx


## -description

Updates the shadow copy storage area maximum size for a certain volume. This may not 
    have an immediate effect. If the <i>bVolatile</i> parameter is <b>FALSE</b>, the change continues even if the computer is rebooted.

## -parameters

### -param pwszVolumeName [in]

The name of the volume that is the source of shadow copies. This volume is associated with a shadow copy storage area 
      on the <i>pwszDiffAreaVolumeName</i> volume.
      

The name of the volume must be in one of the following formats and must include a trailing backslash (\\):
       <ul>
<li>The path of a mounted folder, for example, Y:\MountX\</li>
<li>A drive letter, for example, 
         D:\</li>
<li>A volume GUID path of the form \\?&#92;<i>Volume</i>{<i>GUID</i>}\ (where <i>GUID</i> identifies the volume)</li>
</ul>

### -param pwszDiffAreaVolumeName [in]

The name of the volume that contains the  shadow copy storage  area that is associated with the 
      <i>pwszVolumeName</i> volume.
      

The name of the volume must be in one of the following formats and must include a trailing backslash (\\):
       <ul>
<li>The path of a mounted folder</li>
<li>A drive letter with, for example, 
         D:\</li>
<li>A volume GUID path of the form \\?&#92;<i>Volume</i>{<i>GUID</i>}\ (where <i>GUID</i> identifies the volume)</li>
</ul>

### -param llMaximumDiffSpace [in]

Specifies the maximum size, in bytes, for the shadow copy storage area to use for the volume. If this value is zero, 
      the shadow copy storage area will be deleted. If this value is –1, the maximum size is unlimited.

### -param bVolatile [in]

TRUE to indicate that the effect of calling the <b>ChangeDiffAreaMaximumSizeEx</b> method should not continue if the computer is rebooted; otherwise, <b>FALSE</b>.

The default value is <b>FALSE</b>.

If the <i>llMaximumDiffSpace</i> parameter is zero, the <i>bVolatile</i> parameter must be <b>FALSE</b>.

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
The shadow copy storage area maximum size was successfully changed.

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
An expected provider error has occurred. The error code is logged in the event log. For more information, see 
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

The <b>ChangeDiffAreaMaximumSizeEx</b> method is identical to the <a href="/windows/desktop/api/vsmgmt/nf-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt-changediffareamaximumsize">IVssDifferentialSoftwareSnapshotMgmt::ChangeDiffAreaMaximumSize</a> method except for the <i>bVolatile</i> parameter.

Calling the <b>ChangeDiffAreaMaximumSizeEx</b> method with the <i>bVolatile</i> parameter set to <b>FALSE</b> is the same as calling the <a href="/windows/desktop/api/vsmgmt/nf-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt-changediffareamaximumsize">ChangeDiffAreaMaximumSize</a> method.

<b>ChangeDiffAreaMaximumSizeEx</b> makes the shadow copy storage area explicit, which means that it is not deleted automatically when all shadow copies are deleted.

If the shadow copy storage area does not exist, this method creates it.

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b>If the shadow copy storage area does not exist, this method does not create it.

To create a shadow copy storage area, use the <a href="/windows/desktop/api/vsmgmt/nf-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt-adddiffarea">IVssDifferentialSoftwareSnapshotMgmt::AddDiffArea</a> method.

## -see-also

<a href="/windows/desktop/api/vsmgmt/nn-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt2">IVssDifferentialSoftwareSnapshotMgmt2</a>



<a href="/windows/desktop/api/vsmgmt/nf-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt-changediffareamaximumsize">IVssDifferentialSoftwareSnapshotMgmt::ChangeDiffAreaMaximumSize</a>