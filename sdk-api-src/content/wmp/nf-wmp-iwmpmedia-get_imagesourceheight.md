---
UID: NF:wmp.IWMPMedia.get_imageSourceHeight
title: IWMPMedia::get_imageSourceHeight
author: windows-sdk-content
description: The get_imageSourceHeight method retrieves the height of the current media item in pixels.
old-location: wmp\iwmpmedia_get_imagesourceheight.htm
old-project: WMP
ms.assetid: f39049ad-3641-4885-a8e4-f1e46b181f6e
ms.author: windowssdkdev
ms.date: 05/04/2018
ms.keywords: IWMPMedia interface [Windows Media Player],get_imageSourceHeight method, IWMPMedia.get_imageSourceHeight, IWMPMedia2 interface [Windows Media Player],get_imageSourceHeight method, IWMPMedia2::get_imageSourceHeight, IWMPMedia3 interface [Windows Media Player],get_imageSourceHeight method, IWMPMedia3::get_imageSourceHeight, IWMPMedia::get_imageSourceHeight, IWMPMediaget_imageSourceHeight, get_imageSourceHeight, get_imageSourceHeight method [Windows Media Player], get_imageSourceHeight method [Windows Media Player],IWMPMedia interface, get_imageSourceHeight method [Windows Media Player],IWMPMedia2 interface, get_imageSourceHeight method [Windows Media Player],IWMPMedia3 interface, wmp.iwmpmedia_get_imagesourceheight, wmp/IWMPMedia2::get_imageSourceHeight, wmp/IWMPMedia3::get_imageSourceHeight, wmp/IWMPMedia::get_imageSourceHeight
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
 - IWMPMedia.get_imageSourceHeight
 - IWMPMedia2.get_imageSourceHeight
 - IWMPMedia3.get_imageSourceHeight
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPMedia::get_imageSourceHeight


## -description



The <b>get_imageSourceHeight</b> method retrieves the height of the current media item in pixels.




## -parameters




### -param pHeight [out]

Pointer to a <b>long</b> that specifies the height.


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



If the media item is not the current one, this property returns zero.

Before calling this method, you must have read access to the library. For more information, see <a href="https://msdn.microsoft.com/9f722531-a551-4ca9-be5f-01a291a180b0">Library Access</a>.




## -see-also




<a href="https://msdn.microsoft.com/2311067c-b731-47d2-880d-73870fee7694">IWMPMedia Interface</a>
 

 

