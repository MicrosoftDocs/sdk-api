---
UID: NF:wmcontainer.IMFASFMultiplexer.End
title: IMFASFMultiplexer::End (wmcontainer.h)
description: Collects data from the multiplexer and updates the ASF ContentInfo object to include that information in the ASF Header Object.
helpviewer_keywords: ["2a106ea5-976a-40df-a554-1b76d9a07286","End","End method [Media Foundation]","End method [Media Foundation]","IMFASFMultiplexer interface","IMFASFMultiplexer interface [Media Foundation]","End method","IMFASFMultiplexer.End","IMFASFMultiplexer::End","mf.imfasfmultiplexer_end","wmcontainer/IMFASFMultiplexer::End"]
old-location: mf\imfasfmultiplexer_end.htm
tech.root: mf
ms.assetid: 2a106ea5-976a-40df-a554-1b76d9a07286
ms.date: 12/05/2018
ms.keywords: 2a106ea5-976a-40df-a554-1b76d9a07286, End, End method [Media Foundation], End method [Media Foundation],IMFASFMultiplexer interface, IMFASFMultiplexer interface [Media Foundation],End method, IMFASFMultiplexer.End, IMFASFMultiplexer::End, mf.imfasfmultiplexer_end, wmcontainer/IMFASFMultiplexer::End
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
 - IMFASFMultiplexer::End
 - wmcontainer/IMFASFMultiplexer::End
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
 - IMFASFMultiplexer.End
---

# IMFASFMultiplexer::End


## -description

Collects data from the multiplexer and updates the ASF ContentInfo object to include that information in the ASF Header Object.

## -parameters

### -param pIContentInfo [in]

Pointer to the  <a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo">IMFASFContentInfo</a> interface of the ContentInfo object. This must be the same object that was used to initialize the multiplexer. The ContentInfo object represents the ASF Header Object of the file for which the multiplexer generated data packets.

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
<dt><b>MF_E_FLUSH_NEEDED</b></dt>
</dl>
</td>
<td width="60%">
There are pending output media samples waiting in the multiplexer. Call <a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-flush">IMFASFMultiplexer::Flush</a> to force the media samples to be packetized.

</td>
</tr>
</table>

## -remarks

For non-live encoding scenarios (such as encoding to a file), the user should call <b>End</b> to update the specified ContentInfo object, adding data that the multiplexer has collected during the packet generation process. The user should then call <a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generateheader">IMFASFContentInfo::GenerateHeader</a> and write the output header at the beginning of the ASF file (overwriting the header obtained at the beginning of the encoding session). For more information, see <a href="/windows/desktop/medfound/writing-an-asf-header-object-for-a-new-file">Writing an ASF Header Object for a New File</a>.

During live encoding, it is usually not possible to rewrite the header, so this call is not required for live encoding. (The header in those cases will simply lack some of the information that was not available until the end of the encoding session.)

## -see-also

<a href="/windows/desktop/medfound/generating-new-asf-data-packets">Generating New ASF Data Packets</a>



<a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo">IMFASFContentInfo</a>



<a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmultiplexer">IMFASFMultiplexer</a>