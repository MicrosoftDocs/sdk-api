---
UID: NF:vswriter.IVssComponent.AddDirectedTarget
title: IVssComponent::AddDirectedTarget
author: windows-sdk-content
description: The AddDirectedTarget method allows a writer to indicate at restore time that when a file is to be restored, it (the source file) should be remapped.
old-location: base\ivsscomponent_adddirectedtarget.htm
tech.root: VSS
ms.assetid: 927865ff-f3c4-4863-913e-cfffb7bbdbb2
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: AddDirectedTarget, AddDirectedTarget method [VSS], AddDirectedTarget method [VSS],IVssComponent interface, IVssComponent interface [VSS],AddDirectedTarget method, IVssComponent.AddDirectedTarget, IVssComponent::AddDirectedTarget, _win32_ivsscomponent_adddirectedtarget, base.ivsscomponent_adddirectedtarget, vswriter/IVssComponent::AddDirectedTarget
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - VssApi.lib
 - VssApi.dll
api_name:
 - IVssComponent.AddDirectedTarget
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVssComponent::AddDirectedTarget


## -description


The 
<b>AddDirectedTarget</b> method allows a writer to indicate at restore time that when a file is to be restored, it (the source file) should be remapped. The file can be restored to a new restore location and/or ranges of its data restored to different offsets within the restore location.

This method can be called by a writer only during a restore operation.

This method cannot be called while handling a 
<a href="https://msdn.microsoft.com/ee49d4b1-f3f4-4c85-a3a2-f4452d066f21">BackupComplete</a> (<a href="https://msdn.microsoft.com/77d0621d-81bd-4d53-8e5d-f5d3bfd86013">CVssWriter::OnBackupComplete</a>) or <a href="https://msdn.microsoft.com/en-us/library/Aa384652(v=VS.85).aspx">BackupShutdown</a> (<a href="https://msdn.microsoft.com/4b6d5efe-703b-4245-81d8-e2fc7f650d4b">CVssWriter::OnBackupShutdown</a>) event.


## -parameters




### -param wszSourcePath [in]

Null-terminated wide character string containing the path to the directory at restore time containing the file to be restored (the source file). This path should match or be beneath the path of a file set already in the component (or one of its subcomponents if the component defines a component set).


### -param wszSourceFilename [in]

Null-terminated wide character string containing the name of the file (at backup time) that will be remapped at restore time (the source file). The name of the file (<i>wszSourceFilename</i>) cannot contain wildcard characters (* or ?) and must be consistent with the file specification of a file set containing the source path (<i>wszSourcePath</i>).


### -param wszSourceRangeList [in]

A null-terminated wide character string containing a comma-separated list of file offsets and lengths indicating the source file support range (the sections of the file to actually be restored). 




The number and length of the source file support ranges must match the number and size of destination file support ranges.


### -param wszDestinationPath [in]

Null-terminated wide character string containing the path to which source file data will be remapped at restore time.


### -param wszDestinationFilename [in]

Null-terminated wide character string containing the name of the file to which source file data will be remapped at restore time. The name of the file (<i>wszDestinationFilename</i>) cannot contain wildcard characters (* or ?).


### -param wszDestinationRangeList [in]

A null-terminated wide character string containing a comma-separated list of file offsets and lengths indicating the destination file support range (locations to which the sections of the source file are to be restored). 




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
Successfully set the item.

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
<dt><b>VSS_E_BAD_STATE</b></dt>
</dl>
</td>
<td width="60%">
This method was not called by a writer or, if called by a writer, it either was not called during a restore operation or was called while handling a <a href="https://msdn.microsoft.com/en-us/library/Aa384652(v=VS.85).aspx">BackupComplete</a> or <a href="https://msdn.microsoft.com/en-us/library/Aa384652(v=VS.85).aspx">BackupShutdown</a> event.

</td>
</tr>
</table>
 




## -remarks



Only a writer can call 
<b>AddDirectedTarget</b>, and only during restore operations.

A requester will use the directed target information stored in the Backup Components Document only if the restore target is VSS_RT_DIRECTED.

The 
<b>AddDirectedTarget</b> method can be applied to any file managed in the current component or, if the component defines a component set, in any of its nonselectable subcomponents.

Source and destination file specifications may point to the same file. This would allow remapping of a file into itself at restore time.

The syntax of the range listing (<i>wszSourceRanges</i> and <i>wszDestinationRanges</i>) is that of a comma-separated list of the form <b>offset1:length1, offset2:length2</b>, where each offset and length is a 64-bit integer specifying a byte offset and length in bytes, respectively. The offset and length can be expressed either as hexadecimal or decimal values.

The number of entries and their sizes must match in the source and destination range arguments.

<b>AddDirectedTarget</b> can use as its source file any file already managed by the component or one of its subcomponents if the component defines a component set.

Partial files may be added as directed targets, if the partial file ranges to be backed up match the directed target source ranges (see 
<a href="https://msdn.microsoft.com/318dc1ee-e63f-4e79-96b9-8a8bd83facd3">IVssComponent::AddPartialFile</a>). This will allow you to remap partial files at restore time.

In this case, the requester retrieves the directed target information by calling the 
<a href="https://msdn.microsoft.com/e25760b0-14e2-4f1b-b4ff-e7b78f0b7b12">IVssComponent::GetDirectedTarget</a> method and uses that to implement the remapping of the backed-up data during restore.




## -see-also




<a href="https://msdn.microsoft.com/c686a424-b0b9-4efc-8dc6-b92193de2a5d">IVssComponent</a>



<a href="https://msdn.microsoft.com/e25760b0-14e2-4f1b-b4ff-e7b78f0b7b12">IVssComponent::GetDirectedTarget</a>



<a href="https://msdn.microsoft.com/3c8cf80e-66b9-4c6f-a63d-90626937582b">IVssComponent::GetDirectedTargetCount</a>
 

 

