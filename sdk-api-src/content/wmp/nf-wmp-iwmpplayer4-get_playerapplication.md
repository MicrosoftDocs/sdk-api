---
UID: NF:wmp.IWMPPlayer4.get_playerApplication
title: IWMPPlayer4::get_playerApplication (wmp.h)
description: The get_playerApplication method retrieves a pointer to an IWMPPlayerApplication interface when a remoted Windows Media Player control is running.helpviewer_keywords: ["IWMPPlayer4 interface [Windows Media Player]","get_playerApplication method","IWMPPlayer4.get_playerApplication","IWMPPlayer4::get_playerApplication","IWMPPlayer4get_playerApplication","get_playerApplication","get_playerApplication method [Windows Media Player]","get_playerApplication method [Windows Media Player]","IWMPPlayer4 interface","wmp.iwmpplayer4_get_playerapplication","wmp/IWMPPlayer4::get_playerApplication"]
old-location: wmp\iwmpplayer4_get_playerapplication.htm
tech.root: WMP
ms.assetid: 37b4b0b1-f16e-42ed-830e-9b0468a66eeb
ms.date: 12/05/2018
ms.keywords: IWMPPlayer4 interface [Windows Media Player],get_playerApplication method, IWMPPlayer4.get_playerApplication, IWMPPlayer4::get_playerApplication, IWMPPlayer4get_playerApplication, get_playerApplication, get_playerApplication method [Windows Media Player], get_playerApplication method [Windows Media Player],IWMPPlayer4 interface, wmp.iwmpplayer4_get_playerapplication, wmp/IWMPPlayer4::get_playerApplication
f1_keywords:
- wmp/IWMPPlayer4.get_playerApplication
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
- IWMPPlayer4.get_playerApplication
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPPlayer4::get_playerApplication


## -description



The <b>get_playerApplication</b> method retrieves a pointer to an <b>IWMPPlayerApplication</b> interface when a remoted Windows Media Player control is running.




## -parameters




### -param ppIWMPPlayerApplication [out]

Pointer to a pointer to an <b>IWMPPlayerApplication</b> interface.


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



This method is used only when remoting the Windows Media Player control. If the retrieved value is null, the Player control is not embedded in remote mode.

This method is only accessible in C++ code or in script code in skins through the playerApplication global variable.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WMP/global-attributes">Global Attributes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpplayer4">IWMPPlayer4 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpplayerapplication">IWMPPlayerApplication Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/WMP/remoting-the-windows-media-player-control">Remoting the Windows Media Player Control</a>
 

 

