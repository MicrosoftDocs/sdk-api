---
UID: NF:wmcontainer.IMFASFContentInfo.ParseHeader
title: IMFASFContentInfo::ParseHeader (wmcontainer.h)
description: Parses the information in an ASF header and uses that information to set values in the ContentInfo object. You can pass the entire header in a single buffer or send it in several pieces.
helpviewer_keywords: ["149e2514-74e5-403b-925f-53a17dbbcb64","IMFASFContentInfo interface [Media Foundation]","ParseHeader method","IMFASFContentInfo.ParseHeader","IMFASFContentInfo::ParseHeader","ParseHeader","ParseHeader method [Media Foundation]","ParseHeader method [Media Foundation]","IMFASFContentInfo interface","mf.imfasfcontentinfo_parseheader","wmcontainer/IMFASFContentInfo::ParseHeader"]
old-location: mf\imfasfcontentinfo_parseheader.htm
tech.root: mf
ms.assetid: 149e2514-74e5-403b-925f-53a17dbbcb64
ms.date: 12/05/2018
ms.keywords: 149e2514-74e5-403b-925f-53a17dbbcb64, IMFASFContentInfo interface [Media Foundation],ParseHeader method, IMFASFContentInfo.ParseHeader, IMFASFContentInfo::ParseHeader, ParseHeader, ParseHeader method [Media Foundation], ParseHeader method [Media Foundation],IMFASFContentInfo interface, mf.imfasfcontentinfo_parseheader, wmcontainer/IMFASFContentInfo::ParseHeader
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
 - IMFASFContentInfo::ParseHeader
 - wmcontainer/IMFASFContentInfo::ParseHeader
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
 - IMFASFContentInfo.ParseHeader
---

# IMFASFContentInfo::ParseHeader


## -description

Parses the information in an ASF header and uses that information to set values in the ContentInfo object. You can pass the entire header in a single buffer or send it in several pieces.

## -parameters

### -param pIHeaderBuffer [in]

Pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer">IMFMediaBuffer</a> interface of a buffer object containing some or all of the header. The buffer must contain at least 30 bytes, which is the size of the Header Object, not including the objects contained in the Header Object (that is, everything up to and including the Reserved2 field in the Header Object).

### -param cbOffsetWithinHeader [in]

Offset, in bytes, of the first byte in the buffer relative to the beginning of the header.

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
The header is completely parsed and validated.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_ASF_INVALIDDATA</b></dt>
</dl>
</td>
<td width="60%">
The input buffer does not contain valid ASF data.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_BUFFERTOOSMALL</b></dt>
</dl>
</td>
<td width="60%">
The input buffer is too small.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_S_ASF_PARSEINPROGRESS</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded, but the header passed was incomplete. This is the successful return code for all calls but the last one when passing the header in pieces.

</td>
</tr>
</table>

## -remarks

If you pass the header in pieces, the ContentInfo object will keep references to the buffer objects until the entire header is parsed. Therefore, do not write over the buffers passed into this method.

The start of the Header object has the following layout in memory:

<table>
<tr>
<th>Field Name</th>
<th>Size in bytes</th>
</tr>
<tr>
<td>Object ID</td>
<td>16</td>
</tr>
<tr>
<td>Object Size</td>
<td>8</td>
</tr>
<tr>
<td>Number of Header Objects</td>
<td>4</td>
</tr>
<tr>
<td>Reserved1</td>
<td>1</td>
</tr>
<tr>
<td>Reserved2</td>
<td>1</td>
</tr>
</table>
 

The first call to <b>ParseHeader</b> reads everything up to and including Rerserved2, so it requires a minimum of 30 bytes. (Note that the <a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getheadersize">IMFASFContentInfo::GetHeaderSize</a> method reads only the Object ID and Object Size fields, so that method requires a minimum of 24 bytes.)

## -see-also

<a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo">IMFASFContentInfo</a>



<a href="/windows/desktop/medfound/initializing-the-contentinfo-object-of-a-new-asf-file">Initializing the ContentInfo Object of a New ASF File</a>