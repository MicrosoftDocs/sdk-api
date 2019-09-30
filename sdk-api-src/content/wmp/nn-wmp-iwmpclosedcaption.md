---
UID: NN:wmp.IWMPClosedCaption
title: IWMPClosedCaption (wmp.h)
author: windows-sdk-content
description: The IWMPClosedCaption interface provides a way to include captions with a digital media file. The captioning text is in a Synchronized Accessible Media Interchange (SAMI) file.
old-location: wmp\iwmpclosedcaption.htm
tech.root: WMP
ms.assetid: fd67e139-0bc1-459e-b43b-bf07f6f656ed
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWMPClosedCaption, IWMPClosedCaption interface [Windows Media Player], IWMPClosedCaption interface [Windows Media Player],described, IWMPClosedCaptionInterface, wmp.iwmpclosedcaption, wmp/IWMPClosedCaption
ms.topic: interface
f1_keywords: 
 - "wmp/IWMPClosedCaption"
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPClosedCaption interface


## -description



The <b>IWMPClosedCaption</b> interface provides a way to include captions with a digital media file. The captioning text is in a Synchronized Accessible Media Interchange (SAMI) file.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPClosedCaption</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IWMPClosedCaption</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpclosedcaption-get_captioningid">get_captioningId</a>
</td>
<td align="left" width="63%">
Retrieves the name of the frame or control displaying the captioning.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpclosedcaption-get_samifilename">get_SAMIFileName</a>
</td>
<td align="left" width="63%">
Retrieves the name of the file containing the information needed for closed captioning.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpclosedcaption-get_samilang">get_SAMILang</a>
</td>
<td align="left" width="63%">
Retrieves the language displayed for closed captioning.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpclosedcaption-get_samistyle">get_SAMIStyle</a>
</td>
<td align="left" width="63%">
Retrieves the closed captioning style.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpclosedcaption-put_captioningid">put_captioningId</a>
</td>
<td align="left" width="63%">
Specifies the name of the frame or control displaying the captioning.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpclosedcaption-put_samifilename">put_SAMIFileName</a>
</td>
<td align="left" width="63%">
Specifies the name of the file containing the information needed for closed captioning.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpclosedcaption-put_samilang">put_SAMILang</a>
</td>
<td align="left" width="63%">
Specifies the language displayed for closed captioning.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpclosedcaption-put_samistyle">put_SAMIStyle</a>
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
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpcore">IWMPCore</a>
</td>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_closedcaption">get_closedCaption</a>
</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpclosedcaption2">IWMPClosedCaption2 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/WMP/interfaces">Interfaces</a>
 

 

