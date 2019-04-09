---
UID: NF:shlobj_core.IActiveDesktop.GetDesktopItem
title: IActiveDesktop::GetDesktopItem (shlobj_core.h)
author: windows-sdk-content
description: Gets the specified desktop item.
old-location: lwef\iactivedesktop_getdesktopitem.htm
tech.root: lwef
ms.assetid: b9d4a771-023f-4a31-b9b7-39b8b4a8695a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetDesktopItem, GetDesktopItem method [Legacy Windows Environment Features], GetDesktopItem method [Legacy Windows Environment Features],IActiveDesktop interface, IActiveDesktop interface [Legacy Windows Environment Features],GetDesktopItem method, IActiveDesktop.GetDesktopItem, IActiveDesktop::GetDesktopItem, _win32_IActiveDesktop_GetDesktopItem, lwef.iactivedesktop_getdesktopitem, shell.iactivedesktop_getdesktopitem, shlobj_core/IActiveDesktop::GetDesktopItem
ms.topic: method
req.header: shlobj_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.dll: Shell32.dll (version 4.71 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IActiveDesktop.GetDesktopItem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IActiveDesktop::GetDesktopItem


## -description


Gets the specified desktop item.


## -parameters




### -param nComponent

Type: <b>int</b>

An unsigned long integer value that contains the desktop item's index. The index values start at zero. Use <a href="https://msdn.microsoft.com/d2bba6f8-4ff0-4978-93ae-46db9ec6ea48">IActiveDesktop::GetDesktopItemCount</a> to retrieve a count on the total number of desktop items. 


### -param pcomp [in, out]

Type: <b>LPCOMPONENT</b>

The address of the <a href="https://msdn.microsoft.com/2692a2d6-1d33-410f-987c-8388c636cae6">COMPONENT</a> structure of the retrieved desktop item. 


### -param dwReserved

Type: <b>DWORD</b>

Reserved. Must be set to zero. 


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The index values will change as desktop items are added and removed from the Active Desktop. Applications cannot assume that an index value will always be associated with a particular desktop item. 




## -see-also




<a href="https://msdn.microsoft.com/4d572b86-36e8-417b-857c-eb477c04c691">IActiveDesktop</a>
 

 

