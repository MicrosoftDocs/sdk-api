---
UID: NF:vswriter.IVssCreateWriterMetadata.SaveAsXML
title: IVssCreateWriterMetadata::SaveAsXML (vswriter.h)
description: The SaveAsXML method saves the Writer Metadata Document that contains a writer's state information to a specified string.
helpviewer_keywords: ["IVssCreateWriterMetadata interface [VSS]","SaveAsXML method","IVssCreateWriterMetadata.SaveAsXML","IVssCreateWriterMetadata::SaveAsXML","SaveAsXML","SaveAsXML method [VSS]","SaveAsXML method [VSS]","IVssCreateWriterMetadata interface","_win32_ivsscreatewritermetadata_saveasxml","base.ivsscreatewritermetadata_saveasxml","vswriter/IVssCreateWriterMetadata::SaveAsXML"]
old-location: base\ivsscreatewritermetadata_saveasxml.htm
tech.root: base
ms.assetid: 0894912b-85e3-4a5b-bf1b-6bbfe8c9e820
ms.date: 12/05/2018
ms.keywords: IVssCreateWriterMetadata interface [VSS],SaveAsXML method, IVssCreateWriterMetadata.SaveAsXML, IVssCreateWriterMetadata::SaveAsXML, SaveAsXML, SaveAsXML method [VSS], SaveAsXML method [VSS],IVssCreateWriterMetadata interface, _win32_ivsscreatewritermetadata_saveasxml, base.ivsscreatewritermetadata_saveasxml, vswriter/IVssCreateWriterMetadata::SaveAsXML
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
 - IVssCreateWriterMetadata::SaveAsXML
 - vswriter/IVssCreateWriterMetadata::SaveAsXML
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
 - IVssCreateWriterMetadata.SaveAsXML
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
</table>

## -see-also

<a href="/windows/desktop/api/vswriter/nl-vswriter-ivsscreatewritermetadata">IVssCreateWriterMetadata</a>