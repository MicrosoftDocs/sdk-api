---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
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
---

# ITrackShellMenu::SetObscured


## -description


Coordinates obscured items on a toolbar with items in a menu.


## -parameters




### -param hwndTB [in]

Type: <b>HWND</b>

A handle to a toolbar control whose buttons have command IDs that correspond to menu IDs in the tracked menu.


### -param punkBand [in]

Type: <b><a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>*</b>

If this parameter points to a COM object that supports the <a href="https://msdn.microsoft.com/46793ae9-936e-4a58-bc34-84396151b4a3">IShellMenu</a> interface, menu items that correspond to visible toolbar buttons are filtered out of the menu so that they do not appear in both places. 
                
                    

If this parameter is <b>NULL</b> or points to a COM object that does not support the <a href="https://msdn.microsoft.com/46793ae9-936e-4a58-bc34-84396151b4a3">IShellMenu</a> interface, then the obscured buttons in the toolbar are added to the shell menu in the position specified in <i>dwSMSetFlags</i>.


### -param dwSMSetFlags [in]

Type: <b>DWORD</b>

One of the following values.



#### SMSET_TOP (0x10000000)

New menu items are added at the top of the menu.



#### SMSET_BOTTOM (0x20000000)

New menu items are added at the bottom of the menu.



#### SMSET_DONTOWN

Reserved; do not use.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Obscured buttons are those buttons that cannot be displayed due to toolbar size limitations. Commonly, to see them you must press the chevron at the end of the toolbar.



