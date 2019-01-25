---
UID: NF:vswriter.IVssCreateExpressWriterMetadata.SaveAsXML
title: IVssCreateExpressWriterMetadata::SaveAsXML
author: windows-sdk-content
description: Stores the Writer Metadata Document that contains an express writer's state information into a specified string.
old-location: base\ivsscreateexpresswritermetadata_saveasxml.htm
tech.root: VSS
ms.assetid: c2a1ba98-74a1-4944-ac31-fec364060a75
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IVssCreateExpressWriterMetadata interface,SaveAsXML method, IVssCreateExpressWriterMetadata.SaveAsXML, IVssCreateExpressWriterMetadata::SaveAsXML, SaveAsXML, SaveAsXML method, SaveAsXML method,IVssCreateExpressWriterMetadata interface, base.ivsscreateexpresswritermetadata_saveasxml, vswriter/IVssCreateExpressWriterMetadata::SaveAsXML
ms.topic: method
req.header: vswriter.h
req.include-header: Vss.h, VsWriter.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - IVssCreateExpressWriterMetadata.SaveAsXML
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVssCreateExpressWriterMetadata::SaveAsXML


## -description


Stores the Writer Metadata Document that contains an express writer's state information into a specified string.


## -parameters




### -param pbstrXML [in]

A pointer to a string to be used to store the Writer Metadata Document that contains a writer's state information.


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
The parameter value is not valid.

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




<a href="https://msdn.microsoft.com/49112cff-9e61-4218-a013-5ae5eb58b534">IVssCreateExpressWriterMetadata</a>
 

 

