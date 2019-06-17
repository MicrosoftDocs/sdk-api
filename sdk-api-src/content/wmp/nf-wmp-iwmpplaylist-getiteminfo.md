---
UID: NF:wmp.IWMPPlaylist.getItemInfo
title: IWMPPlaylist::getItemInfo (wmp.h)
author: windows-sdk-content
description: The getItemInfo method retrieves the value of a playlist attribute specified by name.
old-location: wmp\iwmpplaylist_getiteminfo.htm
tech.root: WMP
ms.assetid: c6763274-01e4-4a2f-9467-150e1964193a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWMPPlaylist interface [Windows Media Player],getItemInfo method, IWMPPlaylist.getItemInfo, IWMPPlaylist::getItemInfo, IWMPPlaylistgetItemInfo, getItemInfo, getItemInfo method [Windows Media Player], getItemInfo method [Windows Media Player],IWMPPlaylist interface, wmp.iwmpplaylist_getiteminfo, wmp/IWMPPlaylist::getItemInfo
ms.topic: method
f1_keywords: ["wmp/IWMPPlaylist.getItemInfo"]
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
 - IWMPPlaylist.getItemInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPPlaylist::getItemInfo


## -description



The <b>getItemInfo</b> method retrieves the value of a playlist attribute specified by name.




## -parameters




### -param bstrName [in]

<b>BSTR</b> containing the name.


### -param pbstrVal [out]

Pointer to a <b>BSTR</b> containing the returned value.


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



Before calling this method, you must have read access to the library. For more information, see <a href="https://docs.microsoft.com/windows/desktop/WMP/library-access">Library Access</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpplaylist">IWMPPlaylist Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpplaylist-setiteminfo">IWMPPlaylist::setItemInfo</a>
 

 

