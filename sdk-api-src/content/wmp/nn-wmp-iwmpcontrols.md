---
UID: NN:wmp.IWMPControls
title: IWMPControls (wmp.h)
description: The IWMPControls interface provides a way to manipulate the playback of a media item.
helpviewer_keywords: ["IWMPControls","IWMPControls interface [Windows Media Player]","IWMPControls interface [Windows Media Player]","described","IWMPControlsInterface","wmp.iwmpcontrols","wmp/IWMPControls"]
old-location: wmp\iwmpcontrols.htm
tech.root: WMP
ms.assetid: 422ac0d8-8e94-4484-802f-cdf4ae482fa8
ms.date: 12/05/2018
ms.keywords: IWMPControls, IWMPControls interface [Windows Media Player], IWMPControls interface [Windows Media Player],described, IWMPControlsInterface, wmp.iwmpcontrols, wmp/IWMPControls
req.header: wmp.h
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
 - IWMPControls
 - wmp/IWMPControls
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.h
api_name:
 - IWMPControls
---

# IWMPControls interface


## -description

The <b>IWMPControls</b> interface provides a way to manipulate the playback of a media item.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPControls</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IWMPControls</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMPControls</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpcontrols-fastforward">fastForward</a>
</td>
<td align="left" width="63%">
Starts fast play of the media item in the forward direction.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpcontrols-fastreverse">fastReverse</a>
</td>
<td align="left" width="63%">
Starts fast play of the media item in the reverse direction.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpcontrols-get_currentitem">get_currentItem</a>
</td>
<td align="left" width="63%">
Retrieves the current media item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpcontrols-get_currentmarker">get_currentMarker</a>
</td>
<td align="left" width="63%">
Retrieves the current marker number.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpcontrols-get_currentposition">get_currentPosition</a>
</td>
<td align="left" width="63%">
Retrieves the current position in the media item in seconds from the beginning.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpcontrols-get_currentpositionstring">get_currentPositionString</a>
</td>
<td align="left" width="63%">
Retrieves the current position in the media item as a <b>string</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpcontrols-get_isavailable">get_isAvailable</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating whether a specified type of information is available or a given action can be performed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpcontrols-next">next</a>
</td>
<td align="left" width="63%">
Sets the current item to the next item in the playlist.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpcontrols-pause">pause</a>
</td>
<td align="left" width="63%">
Pauses playback of the media item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpcontrols-play">play</a>
</td>
<td align="left" width="63%">
Begins playback of the media item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpcontrols-playitem">playItem</a>
</td>
<td align="left" width="63%">
Begins playback of the current media item, or resumes playback of a paused item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpcontrols-previous">previous</a>
</td>
<td align="left" width="63%">
Sets the current item to the previous item in the playlist.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpcontrols-put_currentitem">put_currentItem</a>
</td>
<td align="left" width="63%">
Specifies the current media item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpcontrols-put_currentmarker">put_currentMarker</a>
</td>
<td align="left" width="63%">
Specifies the current marker number.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpcontrols-put_currentposition">put_currentPosition</a>
</td>
<td align="left" width="63%">
Specifies the current position in the media item in seconds from the beginning.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpcontrols-stop">stop</a>
</td>
<td align="left" width="63%">
Stops playback of the media item.

</td>
</tr>
</table> 

Retrieve a pointer to an <b>IWMPControls</b> interface with the following method.

<table>
<tr>
<th>Interface</th>
<th>Method</th>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpcore">IWMPCore</a>
</td>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_controls">get_controls</a>
</td>
</tr>
</table>

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpcontrols2">IWMPControls2 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpcontrols3">IWMPControls3 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/WMP/interfaces">Interfaces</a>

