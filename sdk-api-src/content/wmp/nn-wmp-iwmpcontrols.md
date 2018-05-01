---
UID: NN:wmp.IWMPControls
title: IWMPControls
author: windows-driver-content
description: The IWMPControls interface provides a way to manipulate the playback of a media item.
old-location: wmp\iwmpcontrols.htm
old-project: WMP
ms.assetid: 422ac0d8-8e94-4484-802f-cdf4ae482fa8
ms.author: windowsdriverdev
ms.date: 4/11/2018
ms.keywords: IWMPControls, IWMPControls interface [Windows Media Player], IWMPControls interface [Windows Media Player], described, IWMPControlsInterface, wmp.iwmpcontrols, wmp/IWMPControls
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: WMPSyncState
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wmp.h
api_name:
-	IWMPControls
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPControls interface


## -description



The <b>IWMPControls</b> interface provides a way to manipulate the playback of a media item.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPControls</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IWMPControls</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/a741da8d-f1a2-4a96-acb6-7c40077f6b5e">fastForward</a>
</td>
<td align="left" width="63%">
Starts fast play of the media item in the forward direction.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2adec4c7-7aca-4191-8c6f-61e137188ad9">fastReverse</a>
</td>
<td align="left" width="63%">
Starts fast play of the media item in the reverse direction.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1c2443cd-d7e6-466f-b728-ad04a415d192">get_currentItem</a>
</td>
<td align="left" width="63%">
Retrieves the current media item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/42576961-a9bd-4f64-bf56-a5d6bd07e82f">get_currentMarker</a>
</td>
<td align="left" width="63%">
Retrieves the current marker number.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ba7d42b4-2025-4881-b1eb-98636bb1c5ce">get_currentPosition</a>
</td>
<td align="left" width="63%">
Retrieves the current position in the media item in seconds from the beginning.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8843852b-f98a-469f-8541-44b3c51ebd6c">get_currentPositionString</a>
</td>
<td align="left" width="63%">
Retrieves the current position in the media item as a <b>string</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/702e09f2-e086-45e3-9ae1-b62ec3e9561f">get_isAvailable</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating whether a specified type of information is available or a given action can be performed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926903">next</a>
</td>
<td align="left" width="63%">
Sets the current item to the next item in the playlist.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451189">pause</a>
</td>
<td align="left" width="63%">
Pauses playback of the media item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/45b5634b-6d23-4e61-90e4-ef0cc9d90a14">play</a>
</td>
<td align="left" width="63%">
Begins playback of the media item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8d4282b0-08a9-4c66-ab8b-93429e77e05d">playItem</a>
</td>
<td align="left" width="63%">
Begins playback of the current media item, or resumes playback of a paused item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e26eca59-1e2d-4a1f-b133-e337a934014b">previous</a>
</td>
<td align="left" width="63%">
Sets the current item to the previous item in the playlist.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/190cec53-5cd9-4bd0-b8d9-23c5389fe231">put_currentItem</a>
</td>
<td align="left" width="63%">
Specifies the current media item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b48e50b3-46d2-4994-bbbf-668f4986109a">put_currentMarker</a>
</td>
<td align="left" width="63%">
Specifies the current marker number.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7deedeed-8ce9-4fd7-9825-817204a9cb3e">put_currentPosition</a>
</td>
<td align="left" width="63%">
Specifies the current position in the media item in seconds from the beginning.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn927275">stop</a>
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
<a href="https://msdn.microsoft.com/24fbb34d-4a5e-4a00-85fc-9659a31dc650">IWMPCore</a>
</td>
<td>
<a href="https://msdn.microsoft.com/54d013f1-d71b-4b6a-90b4-0226022a2a0f">get_controls</a>
</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/aadbd924-b583-4136-8d6c-e3c8c0b3872e">IWMPControls2 Interface</a>



<a href="https://msdn.microsoft.com/ee902912-4f09-4f61-9b81-f4bd50ace892">IWMPControls3 Interface</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>
 

 

