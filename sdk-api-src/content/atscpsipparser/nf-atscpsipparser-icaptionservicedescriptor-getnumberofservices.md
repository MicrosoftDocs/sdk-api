---
UID: NF:atscpsipparser.ICaptionServiceDescriptor.GetNumberOfServices
title: ICaptionServiceDescriptor::GetNumberOfServices (atscpsipparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["GetNumberOfServices","GetNumberOfServices method [Microsoft TV Technologies]","GetNumberOfServices method [Microsoft TV Technologies]","ICaptionServiceDescriptor interface","ICaptionServiceDescriptor interface [Microsoft TV Technologies]","GetNumberOfServices method","ICaptionServiceDescriptor.GetNumberOfServices","ICaptionServiceDescriptor::GetNumberOfServices","ICaptionServiceDescriptorGetNumberOfServices","atscpsipparser/ICaptionServiceDescriptor::GetNumberOfServices","mstv.icaptionservicedescriptor_getnumberofservices"]
old-location: mstv\icaptionservicedescriptor_getnumberofservices.htm
tech.root: mstv
ms.assetid: 50c2baff-a355-45a4-8a05-a193e695c448
ms.date: 12/05/2018
ms.keywords: GetNumberOfServices, GetNumberOfServices method [Microsoft TV Technologies], GetNumberOfServices method [Microsoft TV Technologies],ICaptionServiceDescriptor interface, ICaptionServiceDescriptor interface [Microsoft TV Technologies],GetNumberOfServices method, ICaptionServiceDescriptor.GetNumberOfServices, ICaptionServiceDescriptor::GetNumberOfServices, ICaptionServiceDescriptorGetNumberOfServices, atscpsipparser/ICaptionServiceDescriptor::GetNumberOfServices, mstv.icaptionservicedescriptor_getnumberofservices
req.header: atscpsipparser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - ICaptionServiceDescriptor::GetNumberOfServices
 - atscpsipparser/ICaptionServiceDescriptor::GetNumberOfServices
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - atscpsipparser.h
api_name:
 - ICaptionServiceDescriptor.GetNumberOfServices
---

# ICaptionServiceDescriptor::GetNumberOfServices


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetNumberOfServices</b> method returns the number of caption services.

## -parameters

### -param pbVal [out]

Receives the number of caption services.

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
<tr>
<td width="40%">
<dl>
<dt><b>MPEG2_E_INCORRECT_DESCRIPTOR_TAG</b></dt>
</dl>
</td>
<td width="60%">
The table descriptor tag is incorrect.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MPEG2_E_MALFORMED_TABLE</b></dt>
</dl>
</td>
<td width="60%">
The PSIP table is not well formed.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/atscpsipparser/nn-atscpsipparser-icaptionservicedescriptor">ICaptionServiceDescriptor Interface</a>