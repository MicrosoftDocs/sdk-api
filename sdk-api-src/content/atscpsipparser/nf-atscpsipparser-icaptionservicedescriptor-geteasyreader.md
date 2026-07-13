---
UID: NF:atscpsipparser.ICaptionServiceDescriptor.GetEasyReader
title: ICaptionServiceDescriptor::GetEasyReader (atscpsipparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["GetEasyReader","GetEasyReader method [Microsoft TV Technologies]","GetEasyReader method [Microsoft TV Technologies]","ICaptionServiceDescriptor interface","ICaptionServiceDescriptor interface [Microsoft TV Technologies]","GetEasyReader method","ICaptionServiceDescriptor.GetEasyReader","ICaptionServiceDescriptor::GetEasyReader","ICaptionServiceDescriptorGetEasyReader","atscpsipparser/ICaptionServiceDescriptor::GetEasyReader","mstv.icaptionservicedescriptor_geteasyreader"]
old-location: mstv\icaptionservicedescriptor_geteasyreader.htm
tech.root: mstv
ms.assetid: 7ecf31c8-b93e-4c6c-991c-33ce942757ec
ms.date: 12/05/2018
ms.keywords: GetEasyReader, GetEasyReader method [Microsoft TV Technologies], GetEasyReader method [Microsoft TV Technologies],ICaptionServiceDescriptor interface, ICaptionServiceDescriptor interface [Microsoft TV Technologies],GetEasyReader method, ICaptionServiceDescriptor.GetEasyReader, ICaptionServiceDescriptor::GetEasyReader, ICaptionServiceDescriptorGetEasyReader, atscpsipparser/ICaptionServiceDescriptor::GetEasyReader, mstv.icaptionservicedescriptor_geteasyreader
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
 - ICaptionServiceDescriptor::GetEasyReader
 - atscpsipparser/ICaptionServiceDescriptor::GetEasyReader
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
 - ICaptionServiceDescriptor.GetEasyReader
---

# ICaptionServiceDescriptor::GetEasyReader


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetEasyReader</b> method queries whether a caption service contains "Easy Reader" captions.

## -parameters

### -param bIndex [in]

Zero-based index of the caption service. To get the number of caption services, call <a href="/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-icaptionservicedescriptor-getnumberofservices">ICaptionServiceDescriptor::GetNumberOfServices</a>.

### -param pbVal [out]

Receives the easy_reader flag:

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>0</td>
<td>The caption service does not contain "Easy Reader" captions.</td>
</tr>
<tr>
<td>1</td>
<td>The caption service contains "Easy Reader" captions.</td>
</tr>
</table>

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