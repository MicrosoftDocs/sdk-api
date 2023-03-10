---
UID: NF:wmcodecdsp.IToc.SetDescriptor
title: IToc::SetDescriptor (wmcodecdsp.h)
description: The SetDescriptor method associates a descriptor with the table of contents.
helpviewer_keywords: ["IToc interface [Media Foundation]","SetDescriptor method","IToc.SetDescriptor","IToc::SetDescriptor","SetDescriptor","SetDescriptor method [Media Foundation]","SetDescriptor method [Media Foundation]","IToc interface","codecapi.itoc_setdescriptor","mf.itoc_setdescriptor","wmcodecdsp/IToc::SetDescriptor"]
old-location: mf\itoc_setdescriptor.htm
tech.root: mf
ms.assetid: 55208226-fd2d-48e5-887b-34e95309a770
ms.date: 12/05/2018
ms.keywords: IToc interface [Media Foundation],SetDescriptor method, IToc.SetDescriptor, IToc::SetDescriptor, SetDescriptor, SetDescriptor method [Media Foundation], SetDescriptor method [Media Foundation],IToc interface, codecapi.itoc_setdescriptor, mf.itoc_setdescriptor, wmcodecdsp/IToc::SetDescriptor
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
 - IToc::SetDescriptor
 - wmcodecdsp/IToc::SetDescriptor
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
 - IToc.SetDescriptor
---

# IToc::SetDescriptor


## -description

The <b>SetDescriptor</b> method associates a descriptor with the table of contents.

## -parameters

### -param pDescriptor [in]

Pointer to a <a href="/windows/desktop/api/wmcodecdsp/ns-wmcodecdsp-toc_descriptor">TOC_DESCRIPTOR</a> structure that contains the descriptor.

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

<a href="/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itoc-getdescriptor">GetDescriptor</a>



<a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itoc">IToc</a>