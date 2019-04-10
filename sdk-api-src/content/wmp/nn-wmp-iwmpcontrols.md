---
UID: NN:wmp.IWMPControls
title: IWMPControls (wmp.h)
author: windows-sdk-content
description: The IWMPControls interface provides a way to manipulate the playback of a media item.
old-location: wmp\iwmpcontrols.htm
tech.root: WMP
ms.assetid: 422ac0d8-8e94-4484-802f-cdf4ae482fa8
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWMPControls, IWMPControls interface [Windows Media Player], IWMPControls interface [Windows Media Player],described, IWMPControlsInterface, wmp.iwmpcontrols, wmp/IWMPControls
ms.topic: interface
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.h
api_name:
 - IWMPControls
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPControls interface


## -description



The <b>IWMPControls</b> interface provides a way to manipulate the playback of a media item.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPControls</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IWMPControls</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/en-us/library/Dd563195(v=VS.85).aspx">fastForward</a>
</td>
<td align="left" width="63%">
Starts fast play of the media item in the forward direction.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563196(v=VS.85).aspx">fastReverse</a>
</td>
<td align="left" width="63%">
Starts fast play of the media item in the reverse direction.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563197(v=VS.85).aspx">get_currentItem</a>
</td>
<td align="left" width="63%">
Retrieves the current media item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563198(v=VS.85).aspx">get_currentMarker</a>
</td>
<td align="left" width="63%">
Retrieves the current marker number.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563199(v=VS.85).aspx">get_currentPosition</a>
</td>
<td align="left" width="63%">
Retrieves the current position in the media item in seconds from the beginning.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563200(v=VS.85).aspx">get_currentPositionString</a>
</td>
<td align="left" width="63%">
Retrieves the current position in the media item as a <b>string</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563201(v=VS.85).aspx">get_isAvailable</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating whether a specified type of information is available or a given action can be performed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563203(v=VS.85).aspx">next</a>
</td>
<td align="left" width="63%">
Sets the current item to the next item in the playlist.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563204(v=VS.85).aspx">pause</a>
</td>
<td align="left" width="63%">
Pauses playback of the media item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563205(v=VS.85).aspx">play</a>
</td>
<td align="left" width="63%">
Begins playback of the media item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563206(v=VS.85).aspx">playItem</a>
</td>
<td align="left" width="63%">
Begins playback of the current media item, or resumes playback of a paused item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563207(v=VS.85).aspx">previous</a>
</td>
<td align="left" width="63%">
Sets the current item to the previous item in the playlist.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563208(v=VS.85).aspx">put_currentItem</a>
</td>
<td align="left" width="63%">
Specifies the current media item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563209(v=VS.85).aspx">put_currentMarker</a>
</td>
<td align="left" width="63%">
Specifies the current marker number.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563210(v=VS.85).aspx">put_currentPosition</a>
</td>
<td align="left" width="63%">
Specifies the current position in the media item in seconds from the beginning.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563211(v=VS.85).aspx">stop</a>
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
<a href="https://msdn.microsoft.com/en-us/library/Dd563216(v=VS.85).aspx">IWMPCore</a>
</td>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Dd563226(v=VS.85).aspx">get_controls</a>
</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd563180(v=VS.85).aspx">IWMPControls2 Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563183(v=VS.85).aspx">IWMPControls3 Interface</a>



<a href="https://msdn.microsoft.com/68a0bdaf-ae1b-4ba1-817b-a31c68b9fddd">Interfaces</a>
 

 

