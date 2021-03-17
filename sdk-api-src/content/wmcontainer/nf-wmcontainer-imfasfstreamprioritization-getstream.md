---
UID: NF:wmcontainer.IMFASFStreamPrioritization.GetStream
title: IMFASFStreamPrioritization::GetStream (wmcontainer.h)
description: Note  This interface is not implemented in this version of Media Foundation. Retrieves the stream number of a stream in the stream priority list.
helpviewer_keywords: ["460a929b-71bf-4f41-9e7a-af04a8f1c10f","GetStream","GetStream method [Media Foundation]","GetStream method [Media Foundation]","IMFASFStreamPrioritization interface","IMFASFStreamPrioritization interface [Media Foundation]","GetStream method","IMFASFStreamPrioritization.GetStream","IMFASFStreamPrioritization::GetStream","mf.imfasfstreamprioritization_getstream","wmcontainer/IMFASFStreamPrioritization::GetStream"]
old-location: mf\imfasfstreamprioritization_getstream.htm
tech.root: mf
ms.assetid: 460a929b-71bf-4f41-9e7a-af04a8f1c10f
ms.date: 12/05/2018
ms.keywords: 460a929b-71bf-4f41-9e7a-af04a8f1c10f, GetStream, GetStream method [Media Foundation], GetStream method [Media Foundation],IMFASFStreamPrioritization interface, IMFASFStreamPrioritization interface [Media Foundation],GetStream method, IMFASFStreamPrioritization.GetStream, IMFASFStreamPrioritization::GetStream, mf.imfasfstreamprioritization_getstream, wmcontainer/IMFASFStreamPrioritization::GetStream
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
 - IMFASFStreamPrioritization::GetStream
 - wmcontainer/IMFASFStreamPrioritization::GetStream
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
 - IMFASFStreamPrioritization.GetStream
---

# IMFASFStreamPrioritization::GetStream


## -description

<div class="alert"><b>Note</b>  This interface is not implemented in this version of Media Foundation.</div>
<div> </div>
Retrieves the stream number of a stream in the stream priority list.

## -parameters

### -param dwStreamIndex [in]

Zero-based index of the entry to retrieve from the stream priority list. To get the number of entries in the priority list, call <a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamprioritization-getstreamcount">IMFASFStreamPrioritization::GetStreamCount</a>.

### -param pwStreamNumber [out]

Receives the stream number of the stream priority entry.

### -param pwStreamFlags [out]

Receives a Boolean value. If <b>TRUE</b>, the stream is mandatory.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument or the <i>dwStreamIndex</i> parameter is out of range.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamprioritization">IMFASFStreamPrioritization</a>