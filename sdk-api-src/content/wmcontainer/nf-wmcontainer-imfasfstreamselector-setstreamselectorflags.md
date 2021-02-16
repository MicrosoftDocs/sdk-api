---
UID: NF:wmcontainer.IMFASFStreamSelector.SetStreamSelectorFlags
title: IMFASFStreamSelector::SetStreamSelectorFlags (wmcontainer.h)
description: Sets options for the stream selector.
helpviewer_keywords: ["IMFASFStreamSelector interface [Media Foundation]","SetStreamSelectorFlags method","IMFASFStreamSelector.SetStreamSelectorFlags","IMFASFStreamSelector::SetStreamSelectorFlags","SetStreamSelectorFlags","SetStreamSelectorFlags method [Media Foundation]","SetStreamSelectorFlags method [Media Foundation]","IMFASFStreamSelector interface","a2a0f318-0de2-49e0-b8f2-847ab1371752","mf.imfasfstreamselector_setstreamselectorflags","wmcontainer/IMFASFStreamSelector::SetStreamSelectorFlags"]
old-location: mf\imfasfstreamselector_setstreamselectorflags.htm
tech.root: mf
ms.assetid: a2a0f318-0de2-49e0-b8f2-847ab1371752
ms.date: 12/05/2018
ms.keywords: IMFASFStreamSelector interface [Media Foundation],SetStreamSelectorFlags method, IMFASFStreamSelector.SetStreamSelectorFlags, IMFASFStreamSelector::SetStreamSelectorFlags, SetStreamSelectorFlags, SetStreamSelectorFlags method [Media Foundation], SetStreamSelectorFlags method [Media Foundation],IMFASFStreamSelector interface, a2a0f318-0de2-49e0-b8f2-847ab1371752, mf.imfasfstreamselector_setstreamselectorflags, wmcontainer/IMFASFStreamSelector::SetStreamSelectorFlags
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
 - IMFASFStreamSelector::SetStreamSelectorFlags
 - wmcontainer/IMFASFStreamSelector::SetStreamSelectorFlags
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
 - IMFASFStreamSelector.SetStreamSelectorFlags
---

# IMFASFStreamSelector::SetStreamSelectorFlags


## -description

Sets options for the stream selector.

## -parameters

### -param dwStreamSelectorFlags [in]

Bitwise [MFASF_STREAMSELECTOR_FLAGS](./ne-wmcontainer-mfasf_streamselector_flags.md) enumeration specifying the options to use.

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