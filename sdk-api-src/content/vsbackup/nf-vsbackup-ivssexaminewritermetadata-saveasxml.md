---
UID: NF:vsbackup.IVssExamineWriterMetadata.SaveAsXML
title: IVssExamineWriterMetadata::SaveAsXML
author: windows-driver-content
description: The SaveAsXML method saves the Writer Metadata Document that contains a writer's state information to a specified string. This string can be saved as part of a backup operation.
old-location: base\ivssexaminewritermetadata_saveasxml.htm
old-project: VSS
ms.assetid: 146dcd00-e479-40fa-963b-e7111b783822
ms.author: windowsdriverdev
ms.date: 4/17/2018
ms.keywords: IVssExamineWriterMetadata interface [VSS],SaveAsXML method, IVssExamineWriterMetadata.SaveAsXML, IVssExamineWriterMetadata::SaveAsXML, SaveAsXML, SaveAsXML method [VSS], SaveAsXML method [VSS],IVssExamineWriterMetadata interface, _win32_ivssexaminewritermetadata_saveasxml, base.ivssexaminewritermetadata_saveasxml, vsbackup/IVssExamineWriterMetadata::SaveAsXML
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: AMVPSIZE, *LPAMVPSIZE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	VssApi.lib
-	VssApi.dll
api_name:
-	IVssExamineWriterMetadata.SaveAsXML
product: Windows
targetos: Windows
req.lib: VssApi.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVssExamineWriterMetadata::SaveAsXML


## -description


The 
<b>SaveAsXML</b> method saves the Writer Metadata Document that contains a writer's state information to a specified string. This string can be saved as part of a backup operation.


## -parameters




### -param pbstrXML [in]

Pointer to a string to be used to store the Writer Metadata Document that contains a writer's state information.


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
Successfully saved the contents of the XML document in the <i>pbstrXML</i> parameter value.

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
<dt><b>VSS_E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">

        Unexpected error. The error code is logged in the error log file. For more information, see 
        <a href="https://msdn.microsoft.com/6377d937-5739-45f5-9195-5d18be4069ce">Event and Error Handling Under VSS</a>.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not supported until Windows Server 2008 R2 and Windows 7. E_UNEXPECTED is used instead.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/b3aa04d9-7299-4e3a-b092-d07f2de6eefe">IVssExamineWriterMetadata</a>



<a href="https://msdn.microsoft.com/8a508a2c-1c42-4414-9c54-a78d1e1564a0">IVssExamineWriterMetadata::LoadFromXML</a>
 

 

