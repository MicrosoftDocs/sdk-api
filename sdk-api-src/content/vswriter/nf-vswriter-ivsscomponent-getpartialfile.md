---
UID: NF:vswriter.IVssComponent.GetPartialFile
title: IVssComponent::GetPartialFile
author: windows-sdk-content
description: The GetPartialFile method returns information on a partial file associated with this component.
old-location: base\ivsscomponent_getpartialfile.htm
old-project: vss
ms.assetid: ed589ae8-2abb-4c3b-9695-12649fc89818
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetPartialFile, GetPartialFile method [VSS], GetPartialFile method [VSS],IVssComponent interface, IVssComponent interface [VSS],GetPartialFile method, IVssComponent.GetPartialFile, IVssComponent::GetPartialFile, _win32_ivsscomponent_getpartialfile, base.ivsscomponent_getpartialfile, vswriter/IVssComponent::GetPartialFile
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: VSS_WRITERRESTORE_ENUM
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - VssApi.lib
 - VssApi.dll
api_name:
 - IVssComponent.GetPartialFile
product: Windows
targetos: Windows
req.lib: VssApi.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVssComponent::GetPartialFile


## -description


The 
<b>GetPartialFile</b> method returns information on a partial file associated with this component.


## -parameters




### -param iPartialFile [in]

Index number of the partial file. The value of this parameter is an integer from 0 
      to <i>n</i>–1 inclusive, where <i>n</i> is the total number of partial files associated with a given component. The value of <i>n</i> is returned by 
<a href="https://msdn.microsoft.com/7be84c00-49c4-4c44-9c12-7994247726a5">IVssComponent::GetPartialFileCount</a>.


### -param pbstrPath [out]

Pointer to a string containing the path of the partial file. 




Users of this method need to check to determine whether this path ends with a backslash ("\").


### -param pbstrFilename [out]

Pointer to a string containing the name of the partial file.


### -param pbstrRange [out]

A pointer to a string containing either a listing of file offsets and lengths that make up the partial file support range (the sections of the file that were backed up), or the name of a file containing such a list.


### -param pbstrMetadata [out]

Pointer to a string containing any additional metadata required by a writer to validate a partial file restore operation. The information in this metadata string will be opaque to requesters. 




Additional metadata is not required, so <i>pbstrMetadata</i> may also be empty (zero length).


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
<dt><b>VSS_E_BAD_STATE</b></dt>
</dl>
</td>
<td width="60%">
The caller is not in the correct state (either backup or restore) for the operation.

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
<a href="https://msdn.microsoft.com/6377d937-5739-45f5-9195-5d18be4069ce">Event and Error Handling Under VSS</a>.

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



The caller should free the memory held by the <i>pbstrPath</i>, <i>pbstrFilename</i>, <i>pbstrRange</i>, and <i>pbstrMetadata</i> parameters by calling <a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a>.

A range indicates a subsection of a given file that is to be backed up, independent of the rest of the file.

The syntax of the range listing (<i>pbstrRanges</i>) is that of a comma-separated list of the form <b>offset1:length1, offset2:length2</b>, where each offset and length is a 64-bit integer specifying a byte offset and length in bytes, respectively. The offset and length can be expressed either as hexadecimal or decimal values.

If <i>pbstrRanges</i> refers to a file containing all the offsets and lengths (a ranges file), <i>pbstrRanges</i> should contain the full path to the file.

If <i>wszRange</i> refers to a file containing all the offsets and lengths (a ranges file), <i>wszRange</i> should contain the full path to the file.

A ranges file must be a binary file with the following format:

<ol>
<li>A 64-bit integer indicating the number of distinct file ranges that need to be backed up.</li>
<li>Each range expressed as a pair of 64-bit integers: the offset into the file being backed up, in bytes, and the length of data starting from that offset to be backed up.</li>
</ol>
A ranges file should have been backed up along with the partial file and typically is restored to the same location that it was backed up from.

However, the location to which a ranges file is restored might be altered by the requester, which uses 
<a href="https://msdn.microsoft.com/170f9ea0-4846-49d4-ab06-eb1ce580e827">IVssBackupComponents::SetRangesFilePath</a> to indicate this and to update the Backup Components Document so that <i>pbstrRanges</i> indicates the correct ranges file.

A requester would use the ranges information returned by 
<b>GetPartialFile</b> to restore the backed-up sections to the appropriate location within the copy of the file on disk at restore time.




## -see-also




<a href="https://msdn.microsoft.com/170f9ea0-4846-49d4-ab06-eb1ce580e827">IVssBackupComponents::SetRangesFilePath</a>



<a href="https://msdn.microsoft.com/c686a424-b0b9-4efc-8dc6-b92193de2a5d">IVssComponent</a>



<a href="https://msdn.microsoft.com/318dc1ee-e63f-4e79-96b9-8a8bd83facd3">IVssComponent::AddPartialFile</a>



<a href="https://msdn.microsoft.com/7be84c00-49c4-4c44-9c12-7994247726a5">IVssComponent::GetPartialFileCount</a>
 

 

