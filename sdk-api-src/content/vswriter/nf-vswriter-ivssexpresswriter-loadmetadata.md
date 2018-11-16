---
UID: NF:vswriter.IVssExpressWriter.LoadMetadata
title: IVssExpressWriter::LoadMetadata
author: windows-sdk-content
description: Causes VSS to load the writer's metadata from a string instead of the express writer metadata store.
old-location: base\ivssexpresswriter_load.htm
tech.root: VSS
ms.assetid: 2b670278-4589-47b7-a9ad-a24187c39945
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IVssExpressWriter interface,LoadMetadata method, IVssExpressWriter.LoadMetadata, IVssExpressWriter::LoadMetadata, LoadMetadata, LoadMetadata method, LoadMetadata method,IVssExpressWriter interface, base.ivssexpresswriter_load, vswriter/IVssExpressWriter::LoadMetadata
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - VsWriter.h
api_name:
 - IVssExpressWriter.LoadMetadata
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- vswriter.h
: 
- IVssExpressWriter.LoadMetadata
: 
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
<a href="https://msdn.microsoft.com/6377d937-5739-45f5-9195-5d18be4069ce">Event and Error Handling Under VSS</a>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/debb0731-6e24-4320-8236-220e07ec37c3">IVssExpressWriter</a>
 

 

