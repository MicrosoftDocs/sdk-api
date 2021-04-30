---
UID: NF:wmcodecdsp.ITocEntry.GetDescriptor
title: ITocEntry::GetDescriptor (wmcodecdsp.h)
description: The GetDescriptor method retrieves the descriptor, previously set by a call to SetDescriptor, of the entry.
helpviewer_keywords: ["GetDescriptor","GetDescriptor method [Media Foundation]","GetDescriptor method [Media Foundation]","ITocEntry interface","ITocEntry interface [Media Foundation]","GetDescriptor method","ITocEntry.GetDescriptor","ITocEntry::GetDescriptor","codecapi.itocentry_getdescriptor","mf.itocentry_getdescriptor","wmcodecdsp/ITocEntry::GetDescriptor"]
old-location: mf\itocentry_getdescriptor.htm
tech.root: mf
ms.assetid: bb685d4c-c5ec-413f-b279-25216b2bcee8
ms.date: 12/05/2018
ms.keywords: GetDescriptor, GetDescriptor method [Media Foundation], GetDescriptor method [Media Foundation],ITocEntry interface, ITocEntry interface [Media Foundation],GetDescriptor method, ITocEntry.GetDescriptor, ITocEntry::GetDescriptor, codecapi.itocentry_getdescriptor, mf.itocentry_getdescriptor, wmcodecdsp/ITocEntry::GetDescriptor
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
 - ITocEntry::GetDescriptor
 - wmcodecdsp/ITocEntry::GetDescriptor
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
 - ITocEntry.GetDescriptor
---

# ITocEntry::GetDescriptor


## -description

The <b>GetDescriptor</b> method retrieves the descriptor, previously set by a call to <a href="/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocentry-setdescriptor">SetDescriptor</a>, of the entry.

## -parameters

### -param pDescriptor [out]

Pointer to a <a href="/windows/desktop/api/wmcodecdsp/ns-wmcodecdsp-toc_entry_descriptor">TOC_ENTRY_DESCRIPTOR</a> structure that receives the descriptor.

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

<a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentry">ITocEntry</a>



<a href="/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocentry-setdescriptor">SetDescriptor</a>