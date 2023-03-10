---
UID: NF:wmcodecdsp.IToc.GetDescriptor
title: IToc::GetDescriptor (wmcodecdsp.h)
description: The GetDescriptor method retrieves the descriptor, previously set by SetDescriptor, of the table of contents.
helpviewer_keywords: ["GetDescriptor","GetDescriptor method [Media Foundation]","GetDescriptor method [Media Foundation]","IToc interface","IToc interface [Media Foundation]","GetDescriptor method","IToc.GetDescriptor","IToc::GetDescriptor","codecapi.itoc_getdescriptor","mf.itoc_getdescriptor","wmcodecdsp/IToc::GetDescriptor"]
old-location: mf\itoc_getdescriptor.htm
tech.root: mf
ms.assetid: 4568b50f-a777-4c3d-8c71-66737d24b7cd
ms.date: 12/05/2018
ms.keywords: GetDescriptor, GetDescriptor method [Media Foundation], GetDescriptor method [Media Foundation],IToc interface, IToc interface [Media Foundation],GetDescriptor method, IToc.GetDescriptor, IToc::GetDescriptor, codecapi.itoc_getdescriptor, mf.itoc_getdescriptor, wmcodecdsp/IToc::GetDescriptor
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
 - IToc::GetDescriptor
 - wmcodecdsp/IToc::GetDescriptor
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
 - IToc.GetDescriptor
---

# IToc::GetDescriptor


## -description

The <b>GetDescriptor</b> method retrieves the descriptor, previously set by <a href="/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itoc-setdescriptor">SetDescriptor</a>, of the table of contents.

## -parameters

### -param pDescriptor [out]

Pointer to a <a href="/windows/desktop/api/wmcodecdsp/ns-wmcodecdsp-toc_descriptor">TOC_DESCRIPTOR</a> structure that receives the descriptor.

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

<a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itoc">IToc</a>