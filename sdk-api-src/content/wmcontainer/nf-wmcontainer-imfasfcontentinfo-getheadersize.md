---
UID: NF:wmcontainer.IMFASFContentInfo.GetHeaderSize
title: IMFASFContentInfo::GetHeaderSize (wmcontainer.h)
description: Retrieves the size of the header section of an Advanced Systems Format (ASF) file.
helpviewer_keywords: ["GetHeaderSize","GetHeaderSize method [Media Foundation]","GetHeaderSize method [Media Foundation]","IMFASFContentInfo interface","IMFASFContentInfo interface [Media Foundation]","GetHeaderSize method","IMFASFContentInfo.GetHeaderSize","IMFASFContentInfo::GetHeaderSize","c13ee7e6-df59-448f-80c4-04ac7c8c98ed","mf.imfasfcontentinfo_getheadersize","wmcontainer/IMFASFContentInfo::GetHeaderSize"]
old-location: mf\imfasfcontentinfo_getheadersize.htm
tech.root: mf
ms.assetid: c13ee7e6-df59-448f-80c4-04ac7c8c98ed
ms.date: 12/05/2018
ms.keywords: GetHeaderSize, GetHeaderSize method [Media Foundation], GetHeaderSize method [Media Foundation],IMFASFContentInfo interface, IMFASFContentInfo interface [Media Foundation],GetHeaderSize method, IMFASFContentInfo.GetHeaderSize, IMFASFContentInfo::GetHeaderSize, c13ee7e6-df59-448f-80c4-04ac7c8c98ed, mf.imfasfcontentinfo_getheadersize, wmcontainer/IMFASFContentInfo::GetHeaderSize
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
 - IMFASFContentInfo::GetHeaderSize
 - wmcontainer/IMFASFContentInfo::GetHeaderSize
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
 - IMFASFContentInfo.GetHeaderSize
---

# IMFASFContentInfo::GetHeaderSize


## -description

Retrieves the size of the header section of an Advanced Systems Format (ASF) file.

## -parameters

### -param pIStartOfContent [in]

The <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer">IMFMediaBuffer</a> interface of a buffer object containing the beginning of ASF content. The size of the valid data in the buffer must be at least MFASF_MIN_HEADER_BYTES in bytes.

### -param cbHeaderSize [out]

Receives the size, in bytes, of the header section of the content. The value includes the size of the ASF Header Object plus the size of the header section of the Data Object. Therefore, the resulting value is the offset to the start of the data packets in the ASF Data Object.

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
<dt><b>MF_E_ASF_INVALIDDATA</b></dt>
</dl>
</td>
<td width="60%">
The buffer does not contain valid ASF data.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_BUFFERTOOSMALL</b></dt>
</dl>
</td>
<td width="60%">
The buffer does not contain enough valid data.
              

</td>
</tr>
</table>

## -remarks

The header of an ASF file or stream can be passed to the <a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader">IMFASFContentInfo::ParseHeader</a> method to populate the ContentInfo object with the header information.

## -see-also

<a href="/windows/desktop/medfound/asf-contentinfo-object">ASF ContentInfo Object</a>



<a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo">IMFASFContentInfo</a>



<a href="/windows/desktop/medfound/initializing-the-contentinfo-object-of-a-new-asf-file">Initializing the ContentInfo Object of a New ASF File</a>