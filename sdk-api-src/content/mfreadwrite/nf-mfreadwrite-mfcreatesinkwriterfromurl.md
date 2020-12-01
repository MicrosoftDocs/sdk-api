---
UID: NF:mfreadwrite.MFCreateSinkWriterFromURL
title: MFCreateSinkWriterFromURL function (mfreadwrite.h)
description: Creates the sink writer from a URL or byte stream.
helpviewer_keywords: ["MFCreateSinkWriterFromURL","MFCreateSinkWriterFromURL function [Media Foundation]","mf.mfcreatesinkwriterfromurl","mfreadwrite/MFCreateSinkWriterFromURL"]
old-location: mf\mfcreatesinkwriterfromurl.htm
tech.root: mf
ms.assetid: ac6a30c7-5e44-453a-8114-8d7d65332024
ms.date: 12/05/2018
ms.keywords: MFCreateSinkWriterFromURL, MFCreateSinkWriterFromURL function [Media Foundation], mf.mfcreatesinkwriterfromurl, mfreadwrite/MFCreateSinkWriterFromURL
req.header: mfreadwrite.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista and Platform Update Supplement for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfreadwrite.lib
req.dll: Mfreadwrite.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFCreateSinkWriterFromURL
 - mfreadwrite/MFCreateSinkWriterFromURL
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfreadwrite.dll
api_name:
 - MFCreateSinkWriterFromURL
---

# MFCreateSinkWriterFromURL function


## -description

Creates the sink writer from a URL or byte stream.

## -parameters

### -param pwszOutputURL [in]

A null-terminated string that contains the URL of the output file. This parameter can be <b>NULL</b>.

### -param pByteStream [in]

Pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream">IMFByteStream</a> interface of a byte stream. This parameter can be <b>NULL</b>.

If this parameter is a valid pointer, the sink writer writes to the provided byte stream. (The byte stream must be writable.) Otherwise, if <i>pByteStream</i> is <b>NULL</b>, the sink writer creates a new file named <i>pwszOutputURL</i>.

### -param pAttributes [in]

Pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a> interface. You can use this parameter to configure the sink writer. For more information, see <a href="/windows/desktop/medfound/sink-writer-attributes">Sink Writer Attributes</a>. This parameter can be <b>NULL</b>.

### -param ppSinkWriter [out]

Receives a pointer to the <a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwriter">IMFSinkWriter</a> interface. The caller must release the interface.

## -returns

This function can return one of these values.

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
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified URL was not found.

</td>
</tr>
</table>

## -remarks

Call <b>CoInitialize(Ex)</b> and <a href="/windows/desktop/api/mfapi/nf-mfapi-mfstartup">MFStartup</a> before calling this function.

The first three parameters to this function can be <b>NULL</b>; however, only certain combinations are valid:


<table>
<tr>
<th>Description</th>
<th><i>pwszOutputURL</i></th>
<th><i>pByteStream</i></th>
<th><i>pAttributes</i></th>
</tr>
<tr>
<td>Specify a byte stream, with no URL.</td>
<td><b>NULL</b></td>
<td>non-<b>NULL</b></td>
<td>Required (must not be <b>NULL</b>).</td>
</tr>
<tr>
<td>Specify a URL, with no byte stream.</td>
<td>not <b>NULL</b></td>
<td><b>NULL</b></td>
<td>Optional (may be <b>NULL</b>).</td>
</tr>
<tr>
<td>Specify both a URL and a byte stream.</td>
<td>non-<b>NULL</b></td>
<td>non-<b>NULL</b></td>
<td>Optional (may be <b>NULL</b>).</td>
</tr>
</table>
 



The <i>pAttributes</i> parameter is required in the first case and optional in the others.

<ul>
<li>Case 1: Specify a byte stream without a URL. The <i>pAttributes</i> parameter must point to an attribute store that contains the <a href="/windows/desktop/medfound/mf-transcode-containertype">MF_TRANSCODE_CONTAINERTYPE</a> attribute. The sink writer uses the  MF_TRANSCODE_CONTAINERTYPE attribute to determine the type of file container to write, such as ASF or MP4.</li>
<li>Case 2: Specify a URL without a byte stream. The sink writer creates a new file named <i>pwszOutputURL</i>. If <i>pAttributes</i> specifies an attribute store with the <a href="/windows/desktop/medfound/mf-transcode-containertype">MF_TRANSCODE_CONTAINERTYPE</a> attribute, the sink writer uses that attribute to determine the type of file container. Otherwise, if the MF_TRANSCODE_CONTAINERTYPE attribute is absent or <i>pAttributes</i> is <b>NULL</b>, the sink writer uses the file name extension to select the container type; for example, ".asf" for an ASF file.</li>
<li>Case 3: Specify both a URL and a byte stream. The sink writer writes to the byte stream. The URL provided in <i>pwszOutputURL</i> is informational only; the sink writer does not create a new file. If <i>pAttributes</i> specifies an attribute store with the <a href="/windows/desktop/medfound/mf-transcode-containertype">MF_TRANSCODE_CONTAINERTYPE</a> attribute, the sink writer uses that attribute to determine the type of file container. Otherwise, the sink writer uses the file name extension to select the container type. The MF_TRANSCODE_CONTAINERTYPE attribute overrides the URL file name extension in this case.</li>
</ul>
This function is available on Windows Vista if Platform Update Supplement for Windows Vista is installed.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>