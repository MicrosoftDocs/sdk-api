---
UID: NF:wmcodecdsp.ITocEntry.SetDescriptor
title: ITocEntry::SetDescriptor (wmcodecdsp.h)
description: The SetDescriptor method associates a descriptor with the entry.
helpviewer_keywords: ["ITocEntry interface [Media Foundation]","SetDescriptor method","ITocEntry.SetDescriptor","ITocEntry::SetDescriptor","SetDescriptor","SetDescriptor method [Media Foundation]","SetDescriptor method [Media Foundation]","ITocEntry interface","codecapi.itocentry_setdescriptor","mf.itocentry_setdescriptor","wmcodecdsp/ITocEntry::SetDescriptor"]
old-location: mf\itocentry_setdescriptor.htm
tech.root: mf
ms.assetid: 09a366a6-fcb4-4a0b-8df1-795360d147b9
ms.date: 12/05/2018
ms.keywords: ITocEntry interface [Media Foundation],SetDescriptor method, ITocEntry.SetDescriptor, ITocEntry::SetDescriptor, SetDescriptor, SetDescriptor method [Media Foundation], SetDescriptor method [Media Foundation],ITocEntry interface, codecapi.itocentry_setdescriptor, mf.itocentry_setdescriptor, wmcodecdsp/ITocEntry::SetDescriptor
req.header: wmcodecdsp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.dll: Wmvdspa.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITocEntry::SetDescriptor
 - wmcodecdsp/ITocEntry::SetDescriptor
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmvdspa.dll
api_name:
 - ITocEntry.SetDescriptor
---

# ITocEntry::SetDescriptor


## -description

The <b>SetDescriptor</b> method associates a descriptor with the entry.

## -parameters

### -param pDescriptor [in]

Pointer to a <a href="/windows/desktop/api/wmcodecdsp/ns-wmcodecdsp-toc_entry_descriptor">TOC_ENTRY_DESCRIPTOR</a> structure that contains the descriptor.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocentry-getdescriptor">GetDescriptor</a>



<a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentry">ITocEntry</a>