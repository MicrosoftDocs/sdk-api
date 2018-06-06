---
UID: NF:wmp.IWMPErrorItem.get_customUrl
title: IWMPErrorItem::get_customUrl
author: windows-sdk-content
description: The get_customUrl method retrieves the URL of a website that displays specific information about codec download failure.
old-location: wmp\iwmperroritem_get_customurl.htm
old-project: WMP
ms.assetid: 3cf54c10-a06d-49fc-aa8e-e6264ce23061
ms.author: windowssdkdev
ms.date: 05/04/2018
ms.keywords: IWMPErrorItem interface [Windows Media Player],get_customUrl method, IWMPErrorItem.get_customUrl, IWMPErrorItem::get_customUrl, IWMPErrorItemget_customUrl, get_customUrl, get_customUrl method [Windows Media Player], get_customUrl method [Windows Media Player],IWMPErrorItem interface, wmp.iwmperroritem_get_customurl, wmp/IWMPErrorItem::get_customUrl
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WMPSyncState
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.dll
api_name:
 - IWMPErrorItem.get_customUrl
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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




<a href="https://msdn.microsoft.com/4675eebf-80d7-4412-b3f1-ec54b977db31">IWMPErrorItem Interface</a>
 

 

