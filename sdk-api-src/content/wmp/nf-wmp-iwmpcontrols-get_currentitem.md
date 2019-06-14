---
UID: NF:wmp.IWMPControls.get_currentItem
title: IWMPControls::get_currentItem (wmp.h)
author: windows-sdk-content
description: The get_currentItem method retrieves the current media item in a playlist.
old-location: wmp\iwmpcontrols_get_currentitem.htm
tech.root: WMP
ms.assetid: 1c2443cd-d7e6-466f-b728-ad04a415d192
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWMPControls interface [Windows Media Player],get_currentItem method, IWMPControls.get_currentItem, IWMPControls::get_currentItem, IWMPControlsget_currentItem, get_currentItem, get_currentItem method [Windows Media Player], get_currentItem method [Windows Media Player],IWMPControls interface, wmp.iwmpcontrols_get_currentitem, wmp/IWMPControls::get_currentItem
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
 - IWMPControls.get_currentItem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPControls::get_currentItem


## -description



The <b>get_currentItem</b> method retrieves the current media item in a playlist.




## -parameters




### -param ppIWMPMedia [out]

Pointer to a pointer to an <b>IWMPMedia</b> interface.


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



This method works only with items in the current playlist.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpcontrols">IWMPControls Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpcontrols-put_currentitem">IWMPControls::put_currentItem</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpmedia">IWMPMedia Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpplaylistcollection-getbyname">IWMPPlaylistCollection::getByName</a>
 

 

