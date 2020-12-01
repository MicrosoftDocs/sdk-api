---
UID: NF:wmcontainer.IMFASFContentInfo.GenerateHeader
title: IMFASFContentInfo::GenerateHeader (wmcontainer.h)
description: Encodes the data in the MFASFContentInfo object into a binary Advanced Systems Format (ASF) header.
helpviewer_keywords: ["972f5ae7-ad00-4c3b-8ec4-2cef4ce03c4e","GenerateHeader","GenerateHeader method [Media Foundation]","GenerateHeader method [Media Foundation]","IMFASFContentInfo interface","IMFASFContentInfo interface [Media Foundation]","GenerateHeader method","IMFASFContentInfo.GenerateHeader","IMFASFContentInfo::GenerateHeader","mf.imfasfcontentinfo_generateheader","wmcontainer/IMFASFContentInfo::GenerateHeader"]
old-location: mf\imfasfcontentinfo_generateheader.htm
tech.root: mf
ms.assetid: 972f5ae7-ad00-4c3b-8ec4-2cef4ce03c4e
ms.date: 12/05/2018
ms.keywords: 972f5ae7-ad00-4c3b-8ec4-2cef4ce03c4e, GenerateHeader, GenerateHeader method [Media Foundation], GenerateHeader method [Media Foundation],IMFASFContentInfo interface, IMFASFContentInfo interface [Media Foundation],GenerateHeader method, IMFASFContentInfo.GenerateHeader, IMFASFContentInfo::GenerateHeader, mf.imfasfcontentinfo_generateheader, wmcontainer/IMFASFContentInfo::GenerateHeader
req.header: wmcontainer.h
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
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFASFContentInfo::GenerateHeader
 - wmcontainer/IMFASFContentInfo::GenerateHeader
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFASFContentInfo.GenerateHeader
---

# IMFASFContentInfo::GenerateHeader


## -description

Encodes the data in the <b>MFASFContentInfo</b> object into a binary Advanced Systems Format (ASF) header.

## -parameters

### -param pIHeader [in, out]

A pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer">IMFMediaBuffer</a> interface of the buffer object that will receive the encoded header. Set to <b>NULL</b> to retrieve the size of the header.

### -param pcbHeader [out]

Size of the encoded ASF header in bytes. If <i>pIHeader</i> is <b>NULL</b>, this value is set to the buffer size required to hold the encoded header.

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
<dt><b>MF_E_INVALIDREQUEST</b></dt>
</dl>
</td>
<td width="60%">
The ASF Header Objects do not exist for the media that the ContentInfo object holds reference to.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_ASF_INVALIDDATA</b></dt>
</dl>
</td>
<td width="60%">
The ASF Header Object size exceeds 10 MB.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_BUFFERTOOSMALL</b></dt>
</dl>
</td>
<td width="60%">
The buffer passed in <i>pIHeader</i> is not large enough to hold the ASF Header Object information.
              

</td>
</tr>
</table>

## -remarks

The size received in the <i>pcbHeader</i> parameter includes the padding size. The content information shrinks or expands the padding data depending on the size of the ASF Header Objects.

During this call, the stream properties are set based on the encoding properties of the profile. These properties are available through the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfmetadata">IMFMetadata</a> interface.

## -see-also

<a href="/windows/desktop/medfound/asf-contentinfo-object">ASF ContentInfo Object</a>



<a href="/windows/desktop/medfound/generating-a-new-asf-header-object">Generating a New ASF Header Object</a>



<a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo">IMFASFContentInfo</a>