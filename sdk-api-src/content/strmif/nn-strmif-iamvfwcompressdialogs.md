---
UID: NN:strmif.IAMVfwCompressDialogs
title: IAMVfwCompressDialogs (strmif.h)
description: The IAMVfwCompressDialogs interface displays a dialog box provided by a Video for Windows (VFW) codec.
helpviewer_keywords: ["IAMVfwCompressDialogs","IAMVfwCompressDialogs interface [DirectShow]","IAMVfwCompressDialogs interface [DirectShow]","described","IAMVfwCompressDialogsInterface","dshow.iamvfwcompressdialogs","strmif/IAMVfwCompressDialogs"]
old-location: dshow\iamvfwcompressdialogs.htm
tech.root: dshow
ms.assetid: 5cc23d68-e0e6-401a-8d16-63c8c68af241
ms.date: 12/05/2018
ms.keywords: IAMVfwCompressDialogs, IAMVfwCompressDialogs interface [DirectShow], IAMVfwCompressDialogs interface [DirectShow],described, IAMVfwCompressDialogsInterface, dshow.iamvfwcompressdialogs, strmif/IAMVfwCompressDialogs
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAMVfwCompressDialogs
 - strmif/IAMVfwCompressDialogs
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMVfwCompressDialogs
---

# IAMVfwCompressDialogs interface


## -description

The <code>IAMVfwCompressDialogs</code> interface displays a dialog box provided by a Video for Windows (VFW) codec. The <a href="/windows/desktop/DirectShow/avi-compressor-filter">AVI Compressor</a> filter implements this interface. Applications can use it to display one of the dialog boxes (Configure or About) provided by VFW codecs, and to set and retrieve compressor status.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMVfwCompressDialogs</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAMVfwCompressDialogs</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAMVfwCompressDialogs</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/strmif/nf-strmif-iamvfwcompressdialogs-getstate">GetState</a>
</td>
<td align="left" width="63%">
Retrieves the current configuration settings for the VCM codec currently being used.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/strmif/nf-strmif-iamvfwcompressdialogs-senddrivermessage">SendDriverMessage</a>
</td>
<td align="left" width="63%">
Sends a driver-specific message.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/strmif/nf-strmif-iamvfwcompressdialogs-setstate">SetState</a>
</td>
<td align="left" width="63%">
Sets configuration for the VCM codec.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/strmif/nf-strmif-iamvfwcompressdialogs-showdialog">ShowDialog</a>
</td>
<td align="left" width="63%">
Displays the specified dialog box.

</td>
</tr>
</table>