---
UID: NF:vswriter.IVssComponent.GetDirectedTarget
title: IVssComponent::GetDirectedTarget (vswriter.h)
description: The GetDirectedTarget method returns information stored by a writer, at backup time, to the Backup Components Document to indicate that when a file is to be restored, it (the source file) should be remapped.
helpviewer_keywords: ["GetDirectedTarget","GetDirectedTarget method [VSS]","GetDirectedTarget method [VSS]","IVssComponent interface","IVssComponent interface [VSS]","GetDirectedTarget method","IVssComponent.GetDirectedTarget","IVssComponent::GetDirectedTarget","_win32_ivsscomponent_getdirectedtarget","base.ivsscomponent_getdirectedtarget","vswriter/IVssComponent::GetDirectedTarget"]
old-location: base\ivsscomponent_getdirectedtarget.htm
tech.root: base
ms.assetid: e25760b0-14e2-4f1b-b4ff-e7b78f0b7b12
ms.date: 12/05/2018
ms.keywords: GetDirectedTarget, GetDirectedTarget method [VSS], GetDirectedTarget method [VSS],IVssComponent interface, IVssComponent interface [VSS],GetDirectedTarget method, IVssComponent.GetDirectedTarget, IVssComponent::GetDirectedTarget, _win32_ivsscomponent_getdirectedtarget, base.ivsscomponent_getdirectedtarget, vswriter/IVssComponent::GetDirectedTarget
req.header: vswriter.h
req.include-header: Vss.h, VsWriter.h
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVssComponent::GetDirectedTarget
 - vswriter/IVssComponent::GetDirectedTarget
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
 - IVssComponent.GetDirectedTarget
---

# IVssComponent::GetDirectedTarget


## -description

The 
<b>GetDirectedTarget</b> method returns information stored by a writer, at backup time, to the Backup Components Document to indicate that when a file is to be restored, it (the source file) should be remapped. The file may be restored to a new restore target and/or ranges of its data restored to different locations with the restore target.

Either a writer or a requester can call this method.

## -parameters

### -param iDirectedTarget [in]

Index number of the directed target. The value of this parameter is an integer from 0 
      to <i>n</i>–1 inclusive, where <i>n</i> is the total number of directed targets associated with a given component (and its subcomponents if it defines a component set). The value of <i>n</i> is returned by 
<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-getdirectedtargetcount">IVssComponent::GetDirectedTargetCount</a>.

### -param pbstrSourcePath [out]

The address of a caller-allocated variable that receives a string containing the path to the directory that at backup time contained the file to be restored (the source file). This path should match or be beneath the path of a file set already in the component or one of its subcomponents (if the component defines a component set).

### -param pbstrSourceFileName [out]

The address of a caller-allocated variable that receives a string containing the name of the file (at backup time) that is to be remapped during a restore (the source file). The name of this file should not contain any wildcard characters, and must be a member of the same file set as the source path (<i>pbstrSourcePath</i>).

### -param pbstrSourceRangeList [out]

The address of a caller-allocated variable that receives a string containing a comma-separated list of file offsets and lengths indicating the source file support range (the sections of the file to be restored). 




The number and length of the source file support ranges must match the number and size of destination file support ranges.

### -param pbstrDestinationPath [out]

The address of a caller-allocated variable that receives a string containing the path to which source file data will be remapped at restore time.

### -param pbstrDestinationFilename [out]

The address of a caller-allocated variable that receives a string containing the name of the file to which source file data will be remapped at restore time.

### -param pbstrDestinationRangeList [out]

The address of a caller-allocated variable that receives a string containing a comma-separated list of file offsets and lengths indicating the destination file support range (locations to which the sections of the source file are to be restored). 




The number and length of the destination file support ranges must match the number and size of source file support ranges.

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
Successfully returned the attribute value.

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
<dt><b>VSS_E_INVALID_XML_DOCUMENT</b></dt>
</dl>
</td>
<td width="60%">
The XML document is not valid. Check the event log for details. For more information, see 
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
The specified item was not found.

</td>
</tr>
</table>

## -remarks

If the call to <b>GetDirectedTarget</b> is successful, the caller is responsible for freeing each returned string by calling the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> function.

A requester will use the directed target information stored in the Backup Components Document only if the restore target is VSS_RT_DIRECTED.

The syntax of the range listing (<i>wszSourceRanges</i> and <i>wszDestinationRanges</i>) is that of a comma-separated list of the form <b>offset1:length1, offset2:length2</b>, where each offset and length is a 64-bit integer specifying a byte offset and length in bytes, respectively. The offset and length can be expressed either as hexadecimal or decimal values.

Files whose directed targets are returned by 
<b>GetDirectedTarget</b> may be members of the files of the current component or any subcomponent it defines.

The caller should free the memory held by the <i>pbstrSourcePath</i>, <i>pbstrSourceFileName</i>, <i>pbstrSourceRangeList</i>, <i>pbstrDestinationPath</i>, <i>pbstrDestinationFilename</i>, and <i>pbstrDestinationRangeList</i> parameters by calling <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a>.

Partial files may be added as directed targets, if the partial file ranges to be backed up match the directed target source ranges (see 
<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-addpartialfile">IVssComponent::AddPartialFile</a>). This will allow you to remap partial files.

The requester will need to check if the directed target source file was backed up as a partial file to correctly implement the restore. If this is the case, the requester uses the directed target information in conjunction with the partial file information (<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-getpartialfile">IVssComponent::GetPartialFile</a>) to implement the remapping of the backed-up data during restore.

## -see-also

<a href="/windows/desktop/api/vswriter/nl-vswriter-ivsscomponent">IVssComponent</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-adddirectedtarget">IVssComponent::AddDirectedTarget</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-getdirectedtargetcount">IVssComponent::GetDirectedTargetCount</a>