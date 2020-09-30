---
UID: NF:vswriter.IVssExpressWriter.LoadMetadata
title: IVssExpressWriter::LoadMetadata (vswriter.h)
description: Causes VSS to load the writer's metadata from a string instead of the express writer metadata store.
helpviewer_keywords: ["IVssExpressWriter interface","LoadMetadata method","IVssExpressWriter.LoadMetadata","IVssExpressWriter::LoadMetadata","LoadMetadata","LoadMetadata method","LoadMetadata method","IVssExpressWriter interface","base.ivssexpresswriter_load","vswriter/IVssExpressWriter::LoadMetadata"]
old-location: base\ivssexpresswriter_load.htm
tech.root: base
ms.assetid: 2b670278-4589-47b7-a9ad-a24187c39945
ms.date: 12/05/2018
ms.keywords: IVssExpressWriter interface,LoadMetadata method, IVssExpressWriter.LoadMetadata, IVssExpressWriter::LoadMetadata, LoadMetadata, LoadMetadata method, LoadMetadata method,IVssExpressWriter interface, base.ivssexpresswriter_load, vswriter/IVssExpressWriter::LoadMetadata
req.header: vswriter.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVssExpressWriter::LoadMetadata
 - vswriter/IVssExpressWriter::LoadMetadata
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - VsWriter.h
api_name:
 - IVssExpressWriter.LoadMetadata
---

# IVssExpressWriter::LoadMetadata


## -description

Causes VSS to load the writer's metadata from a string instead of the express writer metadata store.

## -parameters

### -param metadata [in]

A null-terminated wide character string that contains the writer's metadata.

### -param reserved [in]

This parameter is reserved for system use.

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
<dt>0x00000000L</dt>
</dl>
</td>
<td width="60%">
The operation was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_INVALID_XML_DOCUMENT</b></dt>
<dt>0x80042311L</dt>
</dl>
</td>
<td width="60%">
The XML document is not valid. Check the event log for details. For more information, see 
<a href="/windows/desktop/VSS/event-and-error-handling-under-vss">Event and Error Handling Under VSS</a>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/vswriter/nl-vswriter-ivssexpresswriter">IVssExpressWriter</a>