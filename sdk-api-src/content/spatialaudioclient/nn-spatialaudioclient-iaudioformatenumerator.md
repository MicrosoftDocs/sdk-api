---
UID: NN:spatialaudioclient.IAudioFormatEnumerator
title: IAudioFormatEnumerator (spatialaudioclient.h)
description: Provides a list of supported audio formats. The most preferred format is first in the list. Get a reference to this interface by calling ISpatialAudioClient::GetSupportedAudioObjectFormatEnumerator.
helpviewer_keywords: ["IAudioFormatEnumerator","IAudioFormatEnumerator interface [Core Audio]","IAudioFormatEnumerator interface [Core Audio]","described","coreaudio.iaudioformatenumerator","spatialaudioclient/IAudioFormatEnumerator"]
old-location: coreaudio\iaudioformatenumerator.htm
tech.root: CoreAudio
ms.assetid: 50434617-E70E-4931-B98E-61650E9DEA7E
ms.date: 12/05/2018
ms.keywords: IAudioFormatEnumerator, IAudioFormatEnumerator interface [Core Audio], IAudioFormatEnumerator interface [Core Audio],described, coreaudio.iaudioformatenumerator, spatialaudioclient/IAudioFormatEnumerator
req.header: spatialaudioclient.h
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
 - IAudioFormatEnumerator
 - spatialaudioclient/IAudioFormatEnumerator
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - spatialaudioclient.h
api_name:
 - IAudioFormatEnumerator
---

# IAudioFormatEnumerator interface


## -description

Provides a list of supported audio formats. The most preferred format is first in the list. Get a reference to this interface by calling <a href="/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-getsupportedaudioobjectformatenumerator">ISpatialAudioClient::GetSupportedAudioObjectFormatEnumerator</a>.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAudioFormatEnumerator</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAudioFormatEnumerator</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAudioFormatEnumerator</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-iaudioformatenumerator-getcount">GetCount</a>
</td>
<td align="left" width="63%">
Gets the number of supported audio formats in the list

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-iaudioformatenumerator-getformat">GetFormat</a>
</td>
<td align="left" width="63%">
Gets the format with the specified index in the list. The formats are listed in order of importance. The most preferable format is first in the list.

</td>
</tr>
</table>