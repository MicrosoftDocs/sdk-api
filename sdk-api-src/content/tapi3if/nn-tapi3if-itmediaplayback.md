---
UID: NN:tapi3if.ITMediaPlayback
title: ITMediaPlayback (tapi3if.h)
description: The ITMediaPlayback interface provides playback-specific methods that allow an application to set and get the list of files to play. This interface is created by calling QueryInterface on ITTerminal.
helpviewer_keywords: ["ITMediaPlayback","ITMediaPlayback interface [TAPI 2.2]","ITMediaPlayback interface [TAPI 2.2]","described","_tapi3_itmediaplayback","tapi3.itmediaplayback","tapi3if/ITMediaPlayback"]
old-location: tapi3\itmediaplayback.htm
tech.root: tapi3
ms.assetid: 66b43721-f902-4a0e-8cbb-418438617f47
ms.date: 12/05/2018
ms.keywords: ITMediaPlayback, ITMediaPlayback interface [TAPI 2.2], ITMediaPlayback interface [TAPI 2.2],described, _tapi3_itmediaplayback, tapi3.itmediaplayback, tapi3if/ITMediaPlayback
f1_keywords:
- tapi3if/ITMediaPlayback
dev_langs:
- c++
req.header: tapi3if.h
req.include-header: Tapi3.h
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
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Tapi3.dll
api_name:
- ITMediaPlayback
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITMediaPlayback interface


## -description


The 
<b>ITMediaPlayback</b> interface provides playback-specific methods that allow an application to set and get the list of files to play. This interface is created by calling <b>QueryInterface</b> on 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itterminal">ITTerminal</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITMediaPlayback</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITMediaPlayback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITMediaPlayback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itmediaplayback-get_playlist">get_PlayList</a>
</td>
<td align="left" width="63%">
Gets the list of files to play.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itmediaplayback-put_playlist">put_PlayList</a>
</td>
<td align="left" width="63%">
Sets the list of files to play.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itmediarecord">ITMediaRecord</a>
 

 

