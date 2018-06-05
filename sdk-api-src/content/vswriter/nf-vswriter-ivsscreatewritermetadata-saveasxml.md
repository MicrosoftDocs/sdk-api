---
UID: NF:vswriter.IVssCreateWriterMetadata.SaveAsXML
title: IVssCreateWriterMetadata::SaveAsXML
author: windows-sdk-content
description: The SaveAsXML method saves the Writer Metadata Document that contains a writer's state information to a specified string.
old-location: base\ivsscreatewritermetadata_saveasxml.htm
old-project: VSS
ms.assetid: 0894912b-85e3-4a5b-bf1b-6bbfe8c9e820
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: IVssCreateWriterMetadata interface [VSS],SaveAsXML method, IVssCreateWriterMetadata.SaveAsXML, IVssCreateWriterMetadata::SaveAsXML, SaveAsXML, SaveAsXML method [VSS], SaveAsXML method [VSS],IVssCreateWriterMetadata interface, _win32_ivsscreatewritermetadata_saveasxml, base.ivsscreatewritermetadata_saveasxml, vswriter/IVssCreateWriterMetadata::SaveAsXML
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	VssApi.lib
-	VssApi.dll
api_name:
-	IVssCreateWriterMetadata.SaveAsXML
product: Windows
targetos: Windows
req.lib: VssApi.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVssCreateWriterMetadata::SaveAsXML


## -description


The 
<b>SaveAsXML</b> method saves the Writer Metadata Document that contains a writer's state information to a specified string.


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
The operation was successful.

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
<a href="https://msdn.microsoft.com/6377d937-5739-45f5-9195-5d18be4069ce">Event and Error Handling Under VSS</a>.

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




<a href="https://msdn.microsoft.com/427ed302-c3b7-483a-aa48-da6fec1160a9">IVssCreateWriterMetadata</a>
 

 

