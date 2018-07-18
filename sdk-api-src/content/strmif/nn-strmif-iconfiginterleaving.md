---
UID: NN:strmif.IConfigInterleaving
title: IConfigInterleaving
author: windows-sdk-content
description: The IConfigInterleaving interface controls how the AVI Mux filter interleaves audio and video samples.
old-location: dshow\iconfiginterleaving.htm
old-project: DirectShow
ms.assetid: 68594752-a711-4372-95db-10947bd2ce39
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: IConfigInterleaving, IConfigInterleaving interface [DirectShow], IConfigInterleaving interface [DirectShow],described, IConfigInterleavingInterface, dshow.iconfiginterleaving, strmif/IConfigInterleaving
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: DVD_RELATIVE_BUTTON
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
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IConfigInterleaving interface


## -description



The <b>IConfigInterleaving</b> interface controls how the <a href="https://msdn.microsoft.com/31d30c91-fc6a-45ec-a2e0-34e6a1e902a4">AVI Mux</a> filter interleaves audio and video samples. Video-authoring applications that handle capturing should use this interface when they need to control how audio samples and video frames will be saved on a disk.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IConfigInterleaving</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IConfigInterleaving</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/659aa136-c7fd-4955-913b-26f7c05325a8">get_Interleaving</a>
</td>
<td align="left" width="63%">
Gets the audio preroll time and the frequency of interleaving

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/02136798-1c49-4181-ad08-d128f580dbd4">get_Mode</a>
</td>
<td align="left" width="63%">
Gets the interleaving quality setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4b1363c4-9cdd-4b28-a5ea-e5e554597be2">put_Interleaving</a>
</td>
<td align="left" width="63%">
Sets the audio preroll time and the frequency of interleaving

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/62b06dc2-2e71-4a14-82e5-63e921a3c11f">put_Mode</a>
</td>
<td align="left" width="63%">
Sets how audio samples and video frames will be saved on disk by specifying quality of interleaving.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>
 

 

