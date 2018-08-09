---
UID: NF:wmp.IWMPSkinManager.SetVisualStyle
title: IWMPSkinManager::SetVisualStyle
author: windows-sdk-content
description: The SetVisualStyle method specifies the path to a theme file in Windows XP to which Windows Media Player synchronizes the skin.
old-location: wmp\iwmpskinmanager_setvisualstyle.htm
old-project: WMP
ms.assetid: 16d0020f-7650-4300-bd34-6f79ecca5175
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IWMPSkinManager interface [Windows Media Player],SetVisualStyle method, IWMPSkinManager.SetVisualStyle, IWMPSkinManager::SetVisualStyle, IWMPSkinManagerSetVisualStyle, SetVisualStyle, SetVisualStyle method [Windows Media Player], SetVisualStyle method [Windows Media Player],IWMPSkinManager interface, wmp.iwmpskinmanager_setvisualstyle, wmp/IWMPSkinManager::SetVisualStyle
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
 - IWMPSkinManager.SetVisualStyle
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPSkinManager::SetVisualStyle


## -description



The <b>SetVisualStyle</b> method specifies the path to a theme file in Windows XP to which Windows Media Player synchronizes the skin.




## -parameters




### -param bstrPath






#### - bstrStyle [in]

<b>BSTR</b> containing the path to the theme file.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>S_OK</td>
<td>The method succeeded.</td>
</tr>
</table>
 




## -remarks



Windows XP calls this method when the user changes the current theme. The current skin selection will change to match the theme, or will change to the Windows Classic skin if there is no skin that matches the current theme. If Windows Media Player is in skin mode, the skin will change immediately. Otherwise, the new skin selection will be applied the next time skin mode is entered.

<b>Windows Media Player 10 Mobile: </b>This method is not supported.




## -see-also




<a href="https://msdn.microsoft.com/c1f27a79-837f-4833-af62-2181406ed725">IWMPSkinManager Interface</a>
 

 

