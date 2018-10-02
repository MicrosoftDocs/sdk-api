---
UID: NF:wmp.IWMPControls.playItem
title: IWMPControls::playItem
author: windows-sdk-content
description: The playItem method plays the specified media item.
old-location: wmp\iwmpcontrols_playitem.htm
tech.root: WMP
ms.assetid: 8d4282b0-08a9-4c66-ab8b-93429e77e05d
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IWMPControls interface [Windows Media Player],playItem method, IWMPControls.playItem, IWMPControls::playItem, IWMPControlsplayItem, playItem, playItem method [Windows Media Player], playItem method [Windows Media Player],IWMPControls interface, wmp.iwmpcontrols_playitem, wmp/IWMPControls::playItem
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
 - IWMPControls.playItem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPControls::playItem


## -description



The <b>playItem</b> method plays the specified media item.




## -parameters




### -param pIWMPMedia [in]

Pointer to an <b>IWMPMedia</b> interface.


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



The media item will load and play automatically, regardless of the value retrieved by the <b>IWMPSettings::get_autoStart</b> method. To load an item without playing it automatically, pass in a <b>VARIANT_BOOL</b> set to <b>FALSE</b> in the <b>IWMPSettings::put_autoStart</b> method and specify a URL in <b>IWMPCore::put_URL</b>, after which <b>IWMPControls::play</b> can be called to start playing the item.

Note
        

<b>playItem</b> works only with items retrieved from <b>IWMPCore::get_currentPlaylist</b>. Calling <b>playItem</b> with a reference to a saved media item is not supported.




## -see-also




<a href="https://msdn.microsoft.com/422ac0d8-8e94-4484-802f-cdf4ae482fa8">IWMPControls Interface</a>



<a href="https://msdn.microsoft.com/45b5634b-6d23-4e61-90e4-ef0cc9d90a14">IWMPControls::play</a>



<a href="https://msdn.microsoft.com/bb923325-67d2-4d73-b7ec-49e9b52cabba">IWMPCore::get_currentPlaylist</a>



<a href="https://msdn.microsoft.com/0a8625b9-19a1-41dc-9bb8-afca4bfebf5a">IWMPCore::put_URL</a>



<a href="https://msdn.microsoft.com/20da6e49-720c-4291-9fb7-def441c7fc66">IWMPPlaylist::get_item</a>



<a href="https://msdn.microsoft.com/37180d0a-8fc4-4fe6-b190-97258803b43b">IWMPSettings::get_autoStart</a>



<a href="https://msdn.microsoft.com/34f80fa4-6e9c-4435-b360-55c2856f89fb">IWMPSettings::put_autoStart</a>
 

 

