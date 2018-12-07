---
UID: NF:wmp.IWMPClosedCaption.get_captioningId
title: IWMPClosedCaption::get_captioningId
author: windows-sdk-content
description: The get_captioningId method retrieves the name of the element displaying the captioning.
old-location: wmp\iwmpclosedcaption_get_captioningid.htm
tech.root: WMP
ms.assetid: c6aa1710-9686-439b-b098-7a3e5da532ee
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMPClosedCaption interface [Windows Media Player],get_captioningId method, IWMPClosedCaption.get_captioningId, IWMPClosedCaption::get_captioningId, IWMPClosedCaptionget_captioningId, get_captioningId, get_captioningId method [Windows Media Player], get_captioningId method [Windows Media Player],IWMPClosedCaption interface, wmp.iwmpclosedcaption_get_captioningid, wmp/IWMPClosedCaption::get_captioningId
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wmp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 9 Series or later.
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
req.dll: Wmp.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.dll
api_name:
 - IWMPClosedCaption.get_captioningId
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPClosedCaption::get_captioningId


## -description



The <b>get_captioningId</b> method retrieves the name of the element displaying the captioning.




## -parameters




### -param pbstrCaptioningID [out]

Pointer to a <b>BSTR</b> containing the captioning ID.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>
 




## -remarks



The element name specified can be any HTML element in the webpage as long as it supports the <b>innerHTML</b> attribute. If the webpage contains multiple frames, the element name can only refer to an element in the same frame as the Windows Media Player control.

<b>Windows Media Player 10 Mobile: </b>This method always retrieves a <b>BSTR</b> containing an empty string.




## -see-also




<a href="https://msdn.microsoft.com/0fdd2cdc-32d4-4fda-9596-b050107abd5f">Adding Closed Captions to Digital Media</a>



<a href="https://msdn.microsoft.com/fd67e139-0bc1-459e-b43b-bf07f6f656ed">IWMPClosedCaption Interface</a>



<a href="https://msdn.microsoft.com/46736a28-e05d-404c-8bad-a51ac58435f0">IWMPClosedCaption::put_captioningId</a>
 

 

