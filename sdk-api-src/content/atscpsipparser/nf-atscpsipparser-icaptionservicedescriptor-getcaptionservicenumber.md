---
UID: NF:atscpsipparser.ICaptionServiceDescriptor.GetCaptionServiceNumber
title: ICaptionServiceDescriptor::GetCaptionServiceNumber (atscpsipparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["GetCaptionServiceNumber","GetCaptionServiceNumber method [Microsoft TV Technologies]","GetCaptionServiceNumber method [Microsoft TV Technologies]","ICaptionServiceDescriptor interface","ICaptionServiceDescriptor interface [Microsoft TV Technologies]","GetCaptionServiceNumber method","ICaptionServiceDescriptor.GetCaptionServiceNumber","ICaptionServiceDescriptor::GetCaptionServiceNumber","ICaptionServiceDescriptorGetCaptionServiceNumber","atscpsipparser/ICaptionServiceDescriptor::GetCaptionServiceNumber","mstv.icaptionservicedescriptor_getcaptionservicenumber"]
old-location: mstv\icaptionservicedescriptor_getcaptionservicenumber.htm
tech.root: mstv
ms.assetid: 0e8ca631-45fd-462c-bab9-4a242751f212
ms.date: 12/05/2018
ms.keywords: GetCaptionServiceNumber, GetCaptionServiceNumber method [Microsoft TV Technologies], GetCaptionServiceNumber method [Microsoft TV Technologies],ICaptionServiceDescriptor interface, ICaptionServiceDescriptor interface [Microsoft TV Technologies],GetCaptionServiceNumber method, ICaptionServiceDescriptor.GetCaptionServiceNumber, ICaptionServiceDescriptor::GetCaptionServiceNumber, ICaptionServiceDescriptorGetCaptionServiceNumber, atscpsipparser/ICaptionServiceDescriptor::GetCaptionServiceNumber, mstv.icaptionservicedescriptor_getcaptionservicenumber
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
 - ICaptionServiceDescriptor::GetCaptionServiceNumber
 - atscpsipparser/ICaptionServiceDescriptor::GetCaptionServiceNumber
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
 - ICaptionServiceDescriptor.GetCaptionServiceNumber
---

# ICaptionServiceDescriptor::GetCaptionServiceNumber


## -description

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetCaptionServiceNumber</b> method returns the service number within the closed captioning stream for a specified caption service.

## -parameters

### -param bIndex [in]

Zero-based index of the caption service. To get the number of caption services, call <a href="/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-icaptionservicedescriptor-getnumberofservices">ICaptionServiceDescriptor::GetNumberOfServices</a>.

### -param pbVal [out]

Receives the caption_service_number field.

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
<tr>
<td width="40%">
<dl>
<dt><b>MPEG2_E_OUT_OF_BOUNDS</b></dt>
</dl>
</td>
<td width="60%">
The <i>bIndex</i> parameter is out of range.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/atscpsipparser/nn-atscpsipparser-icaptionservicedescriptor">ICaptionServiceDescriptor Interface</a>