---
UID: NF:vswriter.IVssComponent.AddPartialFile
title: IVssComponent::AddPartialFile (vswriter.h)
description: The AddPartialFile method indicates that only portions of a given file are to be backed up and which portions those are.
helpviewer_keywords: ["AddPartialFile","AddPartialFile method [VSS]","AddPartialFile method [VSS]","IVssComponent interface","IVssComponent interface [VSS]","AddPartialFile method","IVssComponent.AddPartialFile","IVssComponent::AddPartialFile","_win32_ivsscomponent_addpartialfile","base.ivsscomponent_addpartialfile","vswriter/IVssComponent::AddPartialFile"]
old-location: base\ivsscomponent_addpartialfile.htm
tech.root: base
ms.assetid: 318dc1ee-e63f-4e79-96b9-8a8bd83facd3
ms.date: 12/05/2018
ms.keywords: AddPartialFile, AddPartialFile method [VSS], AddPartialFile method [VSS],IVssComponent interface, IVssComponent interface [VSS],AddPartialFile method, IVssComponent.AddPartialFile, IVssComponent::AddPartialFile, _win32_ivsscomponent_addpartialfile, base.ivsscomponent_addpartialfile, vswriter/IVssComponent::AddPartialFile
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
 - IVssComponent::AddPartialFile
 - vswriter/IVssComponent::AddPartialFile
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
 - IVssComponent.AddPartialFile
---

# IVssComponent::AddPartialFile


## -description

The 
   <b>AddPartialFile</b> method indicates that only
   portions of a given file are to be backed up and which portions those are.

Only a writer can call this method, and only during a backup operation.

## -parameters

### -param wszPath [in]

<b>Null</b>-terminated wide character string containing the path of the file involved in partial file operations. 
     

The path can contain environment variables (for example, %SystemRoot%) but cannot contain wildcard
     characters.

There is no requirement that the path end with a backslash ("\"). It is up to applications that
     retrieve this information to check.

This path should match or be beneath the path of a file set already in the component (or one of its
     subcomponents if the component defines a component set).

### -param wszFilename [in]

<b>Null</b>-terminated wide character string containing the name of the file involved in partial file operations.
     The name of the file (<i>wszFilename</i>) cannot contain wildcard characters (* or ?) and must be consistent with the
     file specification of a file set containing the source path (<i>wszPath</i>).

### -param wszRanges [in]

<b>Null</b>-terminated wide character string containing either a listing of file offsets and lengths that make up
     the partial file support range (the sections of the file to actually be backed up), or the name of a file
     containing such a list. 
     

Specifying the partial file support range is required, and this value cannot be <b>NULL</b>.

### -param wszMetadata [in]

<b>Null</b>-terminated wide character string containing any additional metadata required by a writer to validate a
     partial file restore operation. The information in this metadata string will be opaque to requesters. 
     

If additional metadata is not required, this value can be <b>NULL</b>.

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
The method was not called by a writer or, if called by a writer, was not called during a restore
       operation.

</td>
</tr>
</table>

## -remarks

Only a writer can call this method, and the writer cannot call this method during a restore operation.

The syntax of the range listing (<i>wszRanges</i>) is that of a comma-separated list of the form 
   <b>offset1:length1, offset2:length2</b>, where each offset and length is a 64-bit integer
   specifying a byte offset and length in bytes, respectively. The offset and length can be expressed either as
   hexadecimal or decimal values.

If 
   <i>wszRange</i> refers to a file containing all the offsets and lengths (a ranges file), 
   <i>wszRange</i> will contain only the full path to the file.

A ranges file must be a binary file with the following format:

<ol>
<li>A 64-bit integer indicating the number of distinct file ranges that need to be backed up</li>
<li>Each range expressed as a pair of 64-bit integers: the offset into the file being backed up in bytes, and
     the length of data starting from that offset to be backed up</li>
</ol>
In either case, a range indicates a subsection of a given file that is to be backed up, independent of the rest
   of the file.

Requesters can retrieve the partial file information using 
   <a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-getpartialfile">IVssComponent::GetPartialFile</a> and use the
   offset and length information returned by 
   <b>GetPartialFile</b> to restore backed-up sections to
   the appropriate location within the copy of the file on disk at restore time.

<b>AddPartialFile</b> can be applied to a file already
   managed by the component (or one of its subcomponents if the component defines a component set), or it can add a new
   file to the component and indicate that it will participate in partial file operations.

When indicating that the file to participate is a new file, that file must exist on a shadow-copied volume and
   its path (<i>wszPath</i>) should match or be beneath a path already in the component (or one of its
   subcomponents if the component defines a component set). However, the file's file specification (<i>wszFileSpec</i>) should not match one in the components.

Any newly added files will not support alternate location mappings.

## -see-also

<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-setrangesfilepath">IVssBackupComponents::SetRangesFilePath</a>



<a href="/windows/desktop/api/vswriter/nl-vswriter-ivsscomponent">IVssComponent</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-getpartialfile">IVssComponent::GetPartialFile</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-getpartialfilecount">IVssComponent::GetPartialFileCount</a>