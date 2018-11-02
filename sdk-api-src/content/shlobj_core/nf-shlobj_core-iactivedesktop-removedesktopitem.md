---
UID: NF:shlobj_core.IActiveDesktop.RemoveDesktopItem
title: IActiveDesktop::RemoveDesktopItem
author: windows-sdk-content
description: Removes the specified desktop item from the desktop.
old-location: lwef\iactivedesktop_removedesktopitem.htm
tech.root: lwef
ms.assetid: 6fee6c97-0605-4ad3-90fb-c5271f78536a
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: IActiveDesktop interface [Legacy Windows Environment Features],RemoveDesktopItem method, IActiveDesktop.RemoveDesktopItem, IActiveDesktop::RemoveDesktopItem, RemoveDesktopItem, RemoveDesktopItem method [Legacy Windows Environment Features], RemoveDesktopItem method [Legacy Windows Environment Features],IActiveDesktop interface, _win32_IActiveDesktop_RemoveDesktopItem, lwef.iactivedesktop_removedesktopitem, shell.iactivedesktop_removedesktopitem, shlobj_core/IActiveDesktop::RemoveDesktopItem
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IActiveDesktop.RemoveDesktopItem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IActiveDesktop::RemoveDesktopItem


## -description


Removes the specified desktop item from the desktop.


## -parameters




### -param pcomp [in]

Type: <b>LPCCOMPONENT</b>

The address of the <a href="https://msdn.microsoft.com/2692a2d6-1d33-410f-987c-8388c636cae6">COMPONENT</a> structure that specifies the item to be removed. The desktop item associated with the <b>wszSource</b> member of the structure will be removed. 


### -param dwReserved

Type: <b>DWORD</b>

Reserved. Must be set to zero. 


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/4d572b86-36e8-417b-857c-eb477c04c691">IActiveDesktop</a>
 

 

