---
UID: NN:wmp.IWMPClosedCaption
title: IWMPClosedCaption
author: windows-sdk-content
description: The IWMPClosedCaption interface provides a way to include captions with a digital media file. The captioning text is in a Synchronized Accessible Media Interchange (SAMI) file.
old-location: wmp\iwmpclosedcaption.htm
tech.root: WMP
ms.assetid: fd67e139-0bc1-459e-b43b-bf07f6f656ed
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMPClosedCaption, IWMPClosedCaption interface [Windows Media Player], IWMPClosedCaption interface [Windows Media Player],described, IWMPClosedCaptionInterface, wmp.iwmpclosedcaption, wmp/IWMPClosedCaption
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
 - IWMPClosedCaption
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPClosedCaption interface


## -description



The <b>IWMPClosedCaption</b> interface provides a way to include captions with a digital media file. The captioning text is in a Synchronized Accessible Media Interchange (SAMI) file.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPClosedCaption</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IWMPClosedCaption</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMPClosedCaption</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563121(v=VS.85).aspx">get_captioningId</a>
</td>
<td align="left" width="63%">
Retrieves the name of the frame or control displaying the captioning.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563122(v=VS.85).aspx">get_SAMIFileName</a>
</td>
<td align="left" width="63%">
Retrieves the name of the file containing the information needed for closed captioning.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563123(v=VS.85).aspx">get_SAMILang</a>
</td>
<td align="left" width="63%">
Retrieves the language displayed for closed captioning.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563124(v=VS.85).aspx">get_SAMIStyle</a>
</td>
<td align="left" width="63%">
Retrieves the closed captioning style.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563125(v=VS.85).aspx">put_captioningId</a>
</td>
<td align="left" width="63%">
Specifies the name of the frame or control displaying the captioning.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563126(v=VS.85).aspx">put_SAMIFileName</a>
</td>
<td align="left" width="63%">
Specifies the name of the file containing the information needed for closed captioning.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563127(v=VS.85).aspx">put_SAMILang</a>
</td>
<td align="left" width="63%">
Specifies the language displayed for closed captioning.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563128(v=VS.85).aspx">put_SAMIStyle</a>
</td>
<td align="left" width="63%">
Specifies the closed captioning style.

</td>
</tr>
</table> 

Retrieve a pointer to an <b>IWMPClosedCaption</b> interface with the following method.

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
<a href="https://msdn.microsoft.com/en-us/library/Dd563225(v=VS.85).aspx">get_closedCaption</a>
</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd563114(v=VS.85).aspx">IWMPClosedCaption2 Interface</a>



<a href="https://msdn.microsoft.com/68a0bdaf-ae1b-4ba1-817b-a31c68b9fddd">Interfaces</a>
 

 

