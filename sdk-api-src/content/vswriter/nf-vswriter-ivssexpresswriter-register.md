---
UID: NF:vswriter.IVssExpressWriter.Register
title: IVssExpressWriter::Register (vswriter.h)
description: Causes VSS to store the writer's metadata in the express writer metadata store.
helpviewer_keywords: ["IVssExpressWriter interface","Register method","IVssExpressWriter.Register","IVssExpressWriter::Register","Register","Register method","Register method","IVssExpressWriter interface","base.ivssexpresswriter_register","vswriter/IVssExpressWriter::Register"]
old-location: base\ivssexpresswriter_register.htm
tech.root: base
ms.assetid: 75cdc416-5fb6-4c9e-b7ab-f79b091786b2
ms.date: 12/05/2018
ms.keywords: IVssExpressWriter interface,Register method, IVssExpressWriter.Register, IVssExpressWriter::Register, Register, Register method, Register method,IVssExpressWriter interface, base.ivssexpresswriter_register, vswriter/IVssExpressWriter::Register
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
 - IVssExpressWriter::Register
 - vswriter/IVssExpressWriter::Register
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
 - IVssExpressWriter.Register
---

# IVssExpressWriter::Register


## -description

Causes VSS to store the writer's metadata in the express writer metadata store.



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
<dt><b>VSS_E_OBJECT_ALREADY_EXISTS</b></dt>
<dt>0x8004230DL</dt>
</dl>
</td>
<td width="60%">
Metadata has already been stored for this writer.

</td>
</tr>
</table>

## -remarks

Before using this method, the caller must have either used the <a href="/windows/desktop/api/vswriter/nf-vswriter-ivssexpresswriter-loadmetadata">LoadMetadata</a> method to load the writer's metadata directly or used the <a href="/windows/desktop/api/vswriter/nf-vswriter-ivssexpresswriter-createmetadata">CreateMetadata</a> method to create a writer metadata object.

## -see-also

<a href="/windows/desktop/api/vswriter/nl-vswriter-ivssexpresswriter">IVssExpressWriter</a>
