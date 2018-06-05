---
UID: NF:wmp.IWMPPlayer4.openPlayer
title: IWMPPlayer4::openPlayer
author: windows-sdk-content
description: The openPlayer method opens Windows Media Player using the specified URL.
old-location: wmp\iwmpplayer4_openplayer.htm
old-project: WMP
ms.assetid: e2f08758-cd72-4b6b-bc9c-86f93d1d76c2
ms.author: windowssdkdev
ms.date: 05/04/2018
ms.keywords: IWMPPlayer4 interface [Windows Media Player],openPlayer method, IWMPPlayer4.openPlayer, IWMPPlayer4::openPlayer, IWMPPlayer4openPlayer, openPlayer, openPlayer method [Windows Media Player], openPlayer method [Windows Media Player],IWMPPlayer4 interface, wmp.iwmpplayer4_openplayer, wmp/IWMPPlayer4::openPlayer
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wmp.dll
api_name:
-	IWMPPlayer4.openPlayer
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPPlayer4::openPlayer


## -description



The <b>openPlayer</b> method opens Windows Media Player using the specified URL.




## -parameters




### -param bstrURL [in]

<b>BSTR</b> containing the URL of the media item to play.


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



This method launches Windows Media Player with the specified URL set as the current media item. If the Player was previously closed in skin mode it will open using the skin last chosen by the user. Otherwise, the Player opens in full mode.

If this method is called from a Windows Media Player ActiveX control embedded in remote mode, its behavior is identical to the <b>IWMPPlayerAppication::switchToPlayerApplication</b> method.

<b>Windows Media Player 10 Mobile: </b>This method always returns E_NOTIMPL.




## -see-also




<a href="https://msdn.microsoft.com/afe5dbd1-96e1-4abe-b843-ec6130fa02d0">IWMPPlayer4 Interface</a>



<a href="https://msdn.microsoft.com/cf5a77c5-298e-48de-80cd-d7ecd9e74323">IWMPPlayerAppication::switchToPlayerApplication</a>
 

 

