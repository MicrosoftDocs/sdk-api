---
UID: NF:wmp.IWMPCore.put_currentMedia
title: IWMPCore::put_currentMedia method
author: windows-driver-content
description: The put_currentMedia method specifies the IWMPMedia interface that corresponds to the current media item.
old-location: wmp\iwmpcore_put_currentmedia.htm
old-project: WMP
ms.assetid: 003d1937-13f0-4d2c-ad5c-a83569295b62
ms.author: windowsdriverdev
ms.date: 4/11/2018
ms.keywords: IWMPCore, IWMPCore interface [Windows Media Player], put_currentMedia method, IWMPCore::put_currentMedia, IWMPCoreput_currentMedia, put_currentMedia method [Windows Media Player], put_currentMedia method [Windows Media Player], IWMPCore interface, put_currentMedia,IWMPCore.put_currentMedia, wmp.iwmpcore_put_currentmedia, wmp/IWMPCore::put_currentMedia
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
-	IWMPCore.put_currentMedia
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPCore::put_currentMedia method


## -description



The <b>put_currentMedia</b> method specifies the <b>IWMPMedia</b> interface that corresponds to the current media item.




## -parameters




### -param pMedia [in]

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



If the <b>IWMPSettings::put_autoStart</b> method was invoked with an argument of true, file playback will begin automatically whenever you invoke <b>put_currentMedia</b>.

You can retrieve an <b>IWMPMedia</b> interface for a given media item by invoking the <b>IWMPPlaylist::get_item</b> method.




## -see-also




<a href="https://msdn.microsoft.com/24fbb34d-4a5e-4a00-85fc-9659a31dc650">IWMPCore Interface</a>



<a href="https://msdn.microsoft.com/4f199336-0555-40de-8d27-780b05ef9510">IWMPCore::get_currentMedia</a>



<a href="https://msdn.microsoft.com/2311067c-b731-47d2-880d-73870fee7694">IWMPMedia Interface</a>



<a href="https://msdn.microsoft.com/20da6e49-720c-4291-9fb7-def441c7fc66">IWMPPlaylist::get_item</a>



<a href="https://msdn.microsoft.com/34f80fa4-6e9c-4435-b360-55c2856f89fb">IWMPSettings::put_autoStart</a>
 

 

