---
UID: NF:vswriter.IVssExpressWriter.Unregister
title: IVssExpressWriter::Unregister (vswriter.h)
description: Causes VSS to delete the writer's metadata from the express writer metadata store.
helpviewer_keywords: ["IVssExpressWriter interface","Unregister method","IVssExpressWriter.Unregister","IVssExpressWriter::Unregister","Unregister","Unregister method","Unregister method","IVssExpressWriter interface","base.ivssexpresswriter_unregister","vswriter/IVssExpressWriter::Unregister"]
old-location: base\ivssexpresswriter_unregister.htm
tech.root: base
ms.assetid: 24398ace-4e76-471b-ae04-d2005e09cb6a
ms.date: 12/05/2018
ms.keywords: IVssExpressWriter interface,Unregister method, IVssExpressWriter.Unregister, IVssExpressWriter::Unregister, Unregister, Unregister method, Unregister method,IVssExpressWriter interface, base.ivssexpresswriter_unregister, vswriter/IVssExpressWriter::Unregister
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
 - IVssExpressWriter::Unregister
 - vswriter/IVssExpressWriter::Unregister
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
 - IVssExpressWriter.Unregister
---

# IVssExpressWriter::Unregister


## -description

Causes VSS to delete the writer's metadata from the express writer metadata store.

## -parameters

### -param writerId [in]

The globally unique identifier (GUID) of the writer class.

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
<dt><b>VSS_E_OBJECT_NOT_FOUND</b></dt>
<dt>0x80042308L</dt>
</dl>
</td>
<td width="60%">
The <i>writerId</i> parameter specified a writer that does not exist.

</td>
</tr>
</table>

## -remarks

Before using this method, the caller must have used the <a href="/windows/desktop/api/vswriter/nf-vswriter-ivssexpresswriter-createmetadata">CreateMetadata</a> method to create a writer metadata object.

## -see-also

<a href="/windows/desktop/api/vswriter/nl-vswriter-ivssexpresswriter">IVssExpressWriter</a>