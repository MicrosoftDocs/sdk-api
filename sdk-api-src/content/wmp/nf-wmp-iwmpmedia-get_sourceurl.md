---
UID: NF:wmp.IWMPMedia.get_sourceURL
title: IWMPMedia::get_sourceURL method
author: windows-driver-content
description: The get_sourceURL method retrieves the URL of the media item.
old-location: wmp\iwmpmedia_get_sourceurl.htm
old-project: WMP
ms.assetid: 99a9bd0f-0429-41b0-96fc-b84d895f6b38
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: IWMPMedia, IWMPMedia interface [Windows Media Player], get_sourceURL method, IWMPMedia2 interface [Windows Media Player], get_sourceURL method, IWMPMedia2::get_sourceURL, IWMPMedia3 interface [Windows Media Player], get_sourceURL method, IWMPMedia3::get_sourceURL, IWMPMedia::get_sourceURL, IWMPMediaget_sourceURL, get_sourceURL method [Windows Media Player], get_sourceURL method [Windows Media Player], IWMPMedia interface, get_sourceURL method [Windows Media Player], IWMPMedia2 interface, get_sourceURL method [Windows Media Player], IWMPMedia3 interface, get_sourceURL,IWMPMedia.get_sourceURL, wmp.iwmpmedia_get_sourceurl, wmp/IWMPMedia2::get_sourceURL, wmp/IWMPMedia3::get_sourceURL, wmp/IWMPMedia::get_sourceURL
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
req.typenames: WMPSyncState
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wmp.dll
api_name:
-	IWMPMedia.get_sourceURL
-	IWMPMedia2.get_sourceURL
-	IWMPMedia3.get_sourceURL
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPMedia::get_sourceURL method


## -description



The <b>get_sourceURL</b> method retrieves the URL of the media item.




## -parameters




### -param pbstrSourceURL [out]

Pointer to a <b>BSTR</b> containing the source URL.


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
 




## -see-also




<a href="https://msdn.microsoft.com/2311067c-b731-47d2-880d-73870fee7694">IWMPMedia Interface</a>
 

 

