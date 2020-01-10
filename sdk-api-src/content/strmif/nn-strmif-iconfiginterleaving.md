---
UID: NN:strmif.IConfigInterleaving
title: IConfigInterleaving (strmif.h)
description: The IConfigInterleaving interface controls how the AVI Mux filter interleaves audio and video samples.
old-location: dshow\iconfiginterleaving.htm
tech.root: DirectShow
ms.assetid: 68594752-a711-4372-95db-10947bd2ce39
ms.date: 12/05/2018
ms.keywords: IConfigInterleaving, IConfigInterleaving interface [DirectShow], IConfigInterleaving interface [DirectShow],described, IConfigInterleavingInterface, dshow.iconfiginterleaving, strmif/IConfigInterleaving
f1_keywords:
- strmif/IConfigInterleaving
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
api_name:
- IConfigInterleaving
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IConfigInterleaving interface


## -description



The <b>IConfigInterleaving</b> interface controls how the <a href="https://docs.microsoft.com/windows/desktop/DirectShow/avi-mux-filter">AVI Mux</a> filter interleaves audio and video samples. Video-authoring applications that handle capturing should use this interface when they need to control how audio samples and video frames will be saved on a disk.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IConfigInterleaving</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IConfigInterleaving</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IConfigInterleaving</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iconfiginterleaving-get_interleaving">get_Interleaving</a>
</td>
<td align="left" width="63%">
Gets the audio preroll time and the frequency of interleaving

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iconfiginterleaving-get_mode">get_Mode</a>
</td>
<td align="left" width="63%">
Gets the interleaving quality setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iconfiginterleaving-put_interleaving">put_Interleaving</a>
</td>
<td align="left" width="63%">
Sets the audio preroll time and the frequency of interleaving

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iconfiginterleaving-put_mode">put_Mode</a>
</td>
<td align="left" width="63%">
Sets how audio samples and video frames will be saved on disk by specifying quality of interleaving.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/interfaces">Interfaces</a>
 

 

