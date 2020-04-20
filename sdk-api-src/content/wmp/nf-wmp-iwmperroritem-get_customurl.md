---
UID: NF:wmp.IWMPErrorItem.get_customUrl
title: IWMPErrorItem::get_customUrl (wmp.h)
description: The get_customUrl method retrieves the URL of a website that displays specific information about codec download failure.helpviewer_keywords: ["IWMPErrorItem interface [Windows Media Player]","get_customUrl method","IWMPErrorItem.get_customUrl","IWMPErrorItem::get_customUrl","IWMPErrorItemget_customUrl","get_customUrl","get_customUrl method [Windows Media Player]","get_customUrl method [Windows Media Player]","IWMPErrorItem interface","wmp.iwmperroritem_get_customurl","wmp/IWMPErrorItem::get_customUrl"]
old-location: wmp\iwmperroritem_get_customurl.htm
tech.root: WMP
ms.assetid: 3cf54c10-a06d-49fc-aa8e-e6264ce23061
ms.date: 12/05/2018
ms.keywords: IWMPErrorItem interface [Windows Media Player],get_customUrl method, IWMPErrorItem.get_customUrl, IWMPErrorItem::get_customUrl, IWMPErrorItemget_customUrl, get_customUrl, get_customUrl method [Windows Media Player], get_customUrl method [Windows Media Player],IWMPErrorItem interface, wmp.iwmperroritem_get_customurl, wmp/IWMPErrorItem::get_customUrl
f1_keywords:
- wmp/IWMPErrorItem.get_customUrl
dev_langs:
- c++
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
- IWMPErrorItem.get_customUrl
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPErrorItem::get_customUrl


## -description



The <b>get_customUrl</b> method retrieves the URL of a website that displays specific information about codec download failure.




## -parameters




### -param pbstrCustomUrl [out]

Pointer to a <b>BSTR</b> containing the custom url.


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



<b>Windows Media Player 10 Mobile: </b>This method always retrieves a <b>BSTR</b> containing an empty string.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmperroritem">IWMPErrorItem Interface</a>
 

 

