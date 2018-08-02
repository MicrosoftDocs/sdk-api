---
UID: NF:wmp.IWMPControls.put_currentItem
title: IWMPControls::put_currentItem
author: windows-sdk-content
description: The put_currentItem method specifies the current media item.
old-location: wmp\iwmpcontrols_put_currentitem.htm
old-project: WMP
ms.assetid: 190cec53-5cd9-4bd0-b8d9-23c5389fe231
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IWMPControls interface [Windows Media Player],put_currentItem method, IWMPControls.put_currentItem, IWMPControls::put_currentItem, IWMPControlsput_currentItem, put_currentItem, put_currentItem method [Windows Media Player], put_currentItem method [Windows Media Player],IWMPControls interface, wmp.iwmpcontrols_put_currentitem, wmp/IWMPControls::put_currentItem
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
 - IWMPControls.put_currentItem
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPControls::put_currentItem


## -description



The <b>put_currentItem</b> method specifies the current media item.




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



This method works only with items in the playlist. Calling <b>put_currentItem</b> with a reference to a saved media item is not supported.




## -see-also




<a href="https://msdn.microsoft.com/422ac0d8-8e94-4484-802f-cdf4ae482fa8">IWMPControls Interface</a>



<a href="https://msdn.microsoft.com/1c2443cd-d7e6-466f-b728-ad04a415d192">IWMPControls::get_currentItem</a>



<a href="https://msdn.microsoft.com/2311067c-b731-47d2-880d-73870fee7694">IWMPMedia Interface</a>



<a href="https://msdn.microsoft.com/9d837c57-8612-47ef-a0fa-a3ffa77ac704">IWMPPlaylistCollection::getByName</a>
 

 

