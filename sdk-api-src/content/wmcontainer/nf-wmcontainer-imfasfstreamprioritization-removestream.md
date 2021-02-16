---
UID: NF:wmcontainer.IMFASFStreamPrioritization.RemoveStream
title: IMFASFStreamPrioritization::RemoveStream (wmcontainer.h)
description: Note  This interface is not implemented in this version of Media Foundation. Removes a stream from the stream priority list.
helpviewer_keywords: ["IMFASFStreamPrioritization interface [Media Foundation]","RemoveStream method","IMFASFStreamPrioritization.RemoveStream","IMFASFStreamPrioritization::RemoveStream","RemoveStream","RemoveStream method [Media Foundation]","RemoveStream method [Media Foundation]","IMFASFStreamPrioritization interface","a6139042-9c78-4fe7-8549-655e35be2862","mf.imfasfstreamprioritization_removestream","wmcontainer/IMFASFStreamPrioritization::RemoveStream"]
old-location: mf\imfasfstreamprioritization_removestream.htm
tech.root: mf
ms.assetid: a6139042-9c78-4fe7-8549-655e35be2862
ms.date: 12/05/2018
ms.keywords: IMFASFStreamPrioritization interface [Media Foundation],RemoveStream method, IMFASFStreamPrioritization.RemoveStream, IMFASFStreamPrioritization::RemoveStream, RemoveStream, RemoveStream method [Media Foundation], RemoveStream method [Media Foundation],IMFASFStreamPrioritization interface, a6139042-9c78-4fe7-8549-655e35be2862, mf.imfasfstreamprioritization_removestream, wmcontainer/IMFASFStreamPrioritization::RemoveStream
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
 - IMFASFStreamPrioritization::RemoveStream
 - wmcontainer/IMFASFStreamPrioritization::RemoveStream
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
 - IMFASFStreamPrioritization.RemoveStream
---

# IMFASFStreamPrioritization::RemoveStream


## -description

<div class="alert"><b>Note</b>  This interface is not implemented in this version of Media Foundation.</div>
<div> </div>
Removes a stream from the stream priority list.

## -parameters

### -param dwStreamIndex [in]

Index of the entry in the stream priority list to remove. Values range from zero, to one less than the stream count retrieved by calling <a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamprioritization-getstreamcount">IMFASFStreamPrioritization::GetStreamCount</a>.

## -returns

The method returns an HRESULT. Possible values include, but are not limited to, those in the following table.

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

## -remarks

When a stream is removed from the stream priority list, the index values of all streams that follow it in the list are decremented.

## -see-also

<a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamprioritization">IMFASFStreamPrioritization</a>