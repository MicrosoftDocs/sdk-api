---
UID: NF:wmp.IWMPMedia.get_imageSourceHeight
title: IWMPMedia::get_imageSourceHeight (wmp.h)
description: The get_imageSourceHeight method retrieves the height of the current media item in pixels.
helpviewer_keywords: ["IWMPMedia interface [Windows Media Player]","get_imageSourceHeight method","IWMPMedia.get_imageSourceHeight","IWMPMedia2 interface [Windows Media Player]","get_imageSourceHeight method","IWMPMedia2::get_imageSourceHeight","IWMPMedia3 interface [Windows Media Player]","get_imageSourceHeight method","IWMPMedia3::get_imageSourceHeight","IWMPMedia::get_imageSourceHeight","IWMPMediaget_imageSourceHeight","get_imageSourceHeight","get_imageSourceHeight method [Windows Media Player]","get_imageSourceHeight method [Windows Media Player]","IWMPMedia interface","get_imageSourceHeight method [Windows Media Player]","IWMPMedia2 interface","get_imageSourceHeight method [Windows Media Player]","IWMPMedia3 interface","wmp.iwmpmedia_get_imagesourceheight","wmp/IWMPMedia2::get_imageSourceHeight","wmp/IWMPMedia3::get_imageSourceHeight","wmp/IWMPMedia::get_imageSourceHeight"]
old-location: wmp\iwmpmedia_get_imagesourceheight.htm
tech.root: WMP
ms.assetid: f39049ad-3641-4885-a8e4-f1e46b181f6e
ms.date: 12/05/2018
ms.keywords: IWMPMedia interface [Windows Media Player],get_imageSourceHeight method, IWMPMedia.get_imageSourceHeight, IWMPMedia2 interface [Windows Media Player],get_imageSourceHeight method, IWMPMedia2::get_imageSourceHeight, IWMPMedia3 interface [Windows Media Player],get_imageSourceHeight method, IWMPMedia3::get_imageSourceHeight, IWMPMedia::get_imageSourceHeight, IWMPMediaget_imageSourceHeight, get_imageSourceHeight, get_imageSourceHeight method [Windows Media Player], get_imageSourceHeight method [Windows Media Player],IWMPMedia interface, get_imageSourceHeight method [Windows Media Player],IWMPMedia2 interface, get_imageSourceHeight method [Windows Media Player],IWMPMedia3 interface, wmp.iwmpmedia_get_imagesourceheight, wmp/IWMPMedia2::get_imageSourceHeight, wmp/IWMPMedia3::get_imageSourceHeight, wmp/IWMPMedia::get_imageSourceHeight
f1_keywords:
- wmp/IWMPMedia.get_imageSourceHeight
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
- IWMPMedia.get_imageSourceHeight
- IWMPMedia2.get_imageSourceHeight
- IWMPMedia3.get_imageSourceHeight
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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

Before calling this method, you must have read access to the library. For more information, see <a href="https://docs.microsoft.com/windows/desktop/WMP/library-access">Library Access</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpmedia">IWMPMedia Interface</a>
 

 

