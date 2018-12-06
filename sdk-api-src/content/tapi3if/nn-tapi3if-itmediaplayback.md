---
UID: NN:tapi3if.ITMediaPlayback
title: ITMediaPlayback
author: windows-sdk-content
description: The ITMediaPlayback interface provides playback-specific methods that allow an application to set and get the list of files to play. This interface is created by calling QueryInterface on ITTerminal.
old-location: tapi3\itmediaplayback.htm
tech.root: tapi
ms.assetid: 66b43721-f902-4a0e-8cbb-418438617f47
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITMediaPlayback, ITMediaPlayback interface [TAPI 2.2], ITMediaPlayback interface [TAPI 2.2],described, _tapi3_itmediaplayback, tapi3.itmediaplayback, tapi3if/ITMediaPlayback
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITMediaPlayback interface


## -description


The 
<b>ITMediaPlayback</b> interface provides playback-specific methods that allow an application to set and get the list of files to play. This interface is created by calling <b>QueryInterface</b> on 
<a href="https://msdn.microsoft.com/38bc30fa-3e4e-417a-9d04-931ba2451fa4">ITTerminal</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITMediaPlayback</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>ITMediaPlayback</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/57bc8373-0015-4652-bad7-21497d1fd6ff">get_PlayList</a>
</td>
<td align="left" width="63%">
Gets the list of files to play.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/685712ef-100f-4f8d-9b1f-c43170c0f197">put_PlayList</a>
</td>
<td align="left" width="63%">
Sets the list of files to play.

</td>
</tr>
</table> 


## -see-also




<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>



<a href="https://msdn.microsoft.com/604b0128-1461-40f2-98fe-801dbb71e005">ITMediaRecord</a>
 

 

