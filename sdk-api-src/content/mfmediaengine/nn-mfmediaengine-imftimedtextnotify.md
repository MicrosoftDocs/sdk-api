---
UID: NN:mfmediaengine.IMFTimedTextNotify
title: IMFTimedTextNotify
author: windows-sdk-content
description: Interface that defines callbacks for Microsoft Media Foundation Timed Text notifications.
old-location: mf\imftimedtextnotify.htm
old-project: medfound
ms.assetid: FE782D90-8CD4-4F8B-A20E-CE3F792A2DB4
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: IMFTimedTextNotify, IMFTimedTextNotify interface [Media Foundation], IMFTimedTextNotify interface [Media Foundation],described, mf.imftimedtextnotify, mfmediaengine/IMFTimedTextNotify
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: mfmediaengine.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mfmediaengine.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: MF_MEDIA_ENGINE_KEYERR
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfmediaengine.h
api_name:
 - IMFTimedTextNotify
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFTimedTextNotify interface


## -description


Interface that defines callbacks  for Microsoft Media Foundation Timed Text notifications.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFTimedTextNotify</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFTimedTextNotify</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFTimedTextNotify</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/EE577250-2D75-4130-BA50-95D3E455A574">Cue</a>
</td>
<td align="left" width="63%">
Called when a cue event occurs in a text track.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3658EE26-497D-4D33-BE68-572BCE1B28B1">Error</a>
</td>
<td align="left" width="63%">
Called when an error occurs in a text track.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2743B39A-7C57-418C-897F-5B4952840135">Reset</a>
</td>
<td align="left" width="63%">
Resets the timed-text-notify object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/79F33B32-3C64-4E46-A94E-D0C1BB695AC5">TrackAdded</a>
</td>
<td align="left" width="63%">
Called when a text track is added

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6C88C832-5C18-4196-B142-4E398D498A36">TrackRemoved</a>
</td>
<td align="left" width="63%">
Called when a text track is removed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/C4757863-3D92-4D49-A2CA-8AD7C65461E6">TrackSelected</a>
</td>
<td align="left" width="63%">
Called when a track is selected or deselected.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

