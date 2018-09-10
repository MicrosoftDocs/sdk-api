---
UID: NN:wmp.IWMPClosedCaption
title: IWMPClosedCaption
author: windows-sdk-content
description: The IWMPClosedCaption interface provides a way to include captions with a digital media file. The captioning text is in a Synchronized Accessible Media Interchange (SAMI) file.
old-location: wmp\iwmpclosedcaption.htm
tech.root: WMP
ms.assetid: fd67e139-0bc1-459e-b43b-bf07f6f656ed
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IWMPClosedCaption, IWMPClosedCaption interface [Windows Media Player], IWMPClosedCaption interface [Windows Media Player],described, IWMPClosedCaptionInterface, wmp.iwmpclosedcaption, wmp/IWMPClosedCaption
ms.prod: windows
ms.technology: windows-sdk
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
<a href="https://msdn.microsoft.com/c6aa1710-9686-439b-b098-7a3e5da532ee">get_captioningId</a>
</td>
<td align="left" width="63%">
Retrieves the name of the frame or control displaying the captioning.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2f09df76-3bfc-48ce-881f-c905656ecbbf">get_SAMIFileName</a>
</td>
<td align="left" width="63%">
Retrieves the name of the file containing the information needed for closed captioning.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bcb72cf3-dad2-46b4-9652-349b804cda22">get_SAMILang</a>
</td>
<td align="left" width="63%">
Retrieves the language displayed for closed captioning.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/27040145-af7a-4d09-9c80-e0907df08f01">get_SAMIStyle</a>
</td>
<td align="left" width="63%">
Retrieves the closed captioning style.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/46736a28-e05d-404c-8bad-a51ac58435f0">put_captioningId</a>
</td>
<td align="left" width="63%">
Specifies the name of the frame or control displaying the captioning.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ebc05983-3375-4ace-b192-f427b9685310">put_SAMIFileName</a>
</td>
<td align="left" width="63%">
Specifies the name of the file containing the information needed for closed captioning.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2027d8cd-2528-45ad-9f36-f03cc3001ba7">put_SAMILang</a>
</td>
<td align="left" width="63%">
Specifies the language displayed for closed captioning.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8f9a4f6e-4596-4c4a-ade7-5b7e1b82b229">put_SAMIStyle</a>
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
<a href="https://msdn.microsoft.com/24fbb34d-4a5e-4a00-85fc-9659a31dc650">IWMPCore</a>
</td>
<td>
<a href="https://msdn.microsoft.com/7f170430-2ce4-490b-9163-f39221a8db5c">get_closedCaption</a>
</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/21067ac1-d29e-4f1b-b123-34b24929369a">IWMPClosedCaption2 Interface</a>



<a href="https://msdn.microsoft.com/68a0bdaf-ae1b-4ba1-817b-a31c68b9fddd">Interfaces</a>
 

 

