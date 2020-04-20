---
UID: NF:wmp.IWMPMedia.setItemInfo
title: IWMPMedia::setItemInfo (wmp.h)
description: The setItemInfo method sets the value of the specified attribute for the media item.helpviewer_keywords: ["IWMPMedia interface [Windows Media Player]","setItemInfo method","IWMPMedia.setItemInfo","IWMPMedia2 interface [Windows Media Player]","setItemInfo method","IWMPMedia2::setItemInfo","IWMPMedia3 interface [Windows Media Player]","setItemInfo method","IWMPMedia3::setItemInfo","IWMPMedia::setItemInfo","IWMPMediasetItemInfo","setItemInfo","setItemInfo method [Windows Media Player]","setItemInfo method [Windows Media Player]","IWMPMedia interface","setItemInfo method [Windows Media Player]","IWMPMedia2 interface","setItemInfo method [Windows Media Player]","IWMPMedia3 interface","wmp.iwmpmedia_setiteminfo","wmp/IWMPMedia2::setItemInfo","wmp/IWMPMedia3::setItemInfo","wmp/IWMPMedia::setItemInfo"]
old-location: wmp\iwmpmedia_setiteminfo.htm
tech.root: WMP
ms.assetid: 919fe92f-9519-4229-8097-4970a8f6cc25
ms.date: 12/05/2018
ms.keywords: IWMPMedia interface [Windows Media Player],setItemInfo method, IWMPMedia.setItemInfo, IWMPMedia2 interface [Windows Media Player],setItemInfo method, IWMPMedia2::setItemInfo, IWMPMedia3 interface [Windows Media Player],setItemInfo method, IWMPMedia3::setItemInfo, IWMPMedia::setItemInfo, IWMPMediasetItemInfo, setItemInfo, setItemInfo method [Windows Media Player], setItemInfo method [Windows Media Player],IWMPMedia interface, setItemInfo method [Windows Media Player],IWMPMedia2 interface, setItemInfo method [Windows Media Player],IWMPMedia3 interface, wmp.iwmpmedia_setiteminfo, wmp/IWMPMedia2::setItemInfo, wmp/IWMPMedia3::setItemInfo, wmp/IWMPMedia::setItemInfo
f1_keywords:
- wmp/IWMPMedia.setItemInfo
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
- IWMPMedia.setItemInfo
- IWMPMedia2.setItemInfo
- IWMPMedia3.setItemInfo
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPMedia::setItemInfo


## -description



The <b>setItemInfo</b> method sets the value of the specified attribute for the media item.




## -parameters




### -param bstrItemName [in]

<b>BSTR</b> containing the attribute name.


### -param bstrVal [in]

<b>BSTR</b> containing the new value.


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



The <b>get_attributeCount</b> method retrieves the number of attributes available for a given media item. Index numbers can then be used with the <b>getAttributeName</b> method to determine the names of the built-in attributes that can be used with this method.

Before using this method, use the <b>isReadOnlyItem</b> method to determine whether a particular attribute can be set.

Before calling this method, you must have full access to the library. For more information, see <a href="https://docs.microsoft.com/windows/desktop/WMP/library-access">Library Access</a>.

Note
        

If you embed the Windows Media Player control in your application, file attributes that you change will not be written to the digital media file until the user runs Windows Media Player. If you use the control in a remoted application written in C++, file attributes that you change will be written to the digital media file shortly after you make the changes. In either case, the changes are immediately available to you through the library.

<b>Windows Media Player 10 Mobile:</b> This method always returns E_INVALIDARG.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpmedia">IWMPMedia Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpmedia-getattributename">IWMPMedia::getAttributeName</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpmedia-get_attributecount">IWMPMedia::get_attributeCount</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpmedia-isreadonlyitem">IWMPMedia::isReadOnlyItem</a>
 

 

