---
UID: NF:wmcontainer.IMFASFStreamSelector.GetStreamCount
title: IMFASFStreamSelector::GetStreamCount (wmcontainer.h)
description: Retrieves the number of streams that are in the Advanced Systems Format (ASF) content.
helpviewer_keywords: ["GetStreamCount","GetStreamCount method [Media Foundation]","GetStreamCount method [Media Foundation]","IMFASFStreamSelector interface","IMFASFStreamSelector interface [Media Foundation]","GetStreamCount method","IMFASFStreamSelector.GetStreamCount","IMFASFStreamSelector::GetStreamCount","e1e80c32-bfd4-4404-9ccc-05b5077b83a6","mf.imfasfstreamselector_getstreamcount","wmcontainer/IMFASFStreamSelector::GetStreamCount"]
old-location: mf\imfasfstreamselector_getstreamcount.htm
tech.root: mf
ms.assetid: e1e80c32-bfd4-4404-9ccc-05b5077b83a6
ms.date: 12/05/2018
ms.keywords: GetStreamCount, GetStreamCount method [Media Foundation], GetStreamCount method [Media Foundation],IMFASFStreamSelector interface, IMFASFStreamSelector interface [Media Foundation],GetStreamCount method, IMFASFStreamSelector.GetStreamCount, IMFASFStreamSelector::GetStreamCount, e1e80c32-bfd4-4404-9ccc-05b5077b83a6, mf.imfasfstreamselector_getstreamcount, wmcontainer/IMFASFStreamSelector::GetStreamCount
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
 - IMFASFStreamSelector::GetStreamCount
 - wmcontainer/IMFASFStreamSelector::GetStreamCount
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
 - IMFASFStreamSelector.GetStreamCount
---

# IMFASFStreamSelector::GetStreamCount


## -description

Retrieves the number of streams that are in the Advanced Systems Format (ASF) content.

## -parameters

### -param pcStreams [out]

Receives the number of streams in the content.

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
</table>

## -see-also

<a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamselector">IMFASFStreamSelector</a>