---
UID: NF:shlobj_core.IActiveDesktop.GetDesktopItemByID
title: IActiveDesktop::GetDesktopItemByID
author: windows-sdk-content
description: Gets the desktop item that matches the given identification.
old-location: lwef\iactivedesktop_getdesktopitembyid.htm
tech.root: lwef
ms.assetid: 44e5fc48-b50d-4410-87c8-7e42634218bf
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetDesktopItemByID, GetDesktopItemByID method [Legacy Windows Environment Features], GetDesktopItemByID method [Legacy Windows Environment Features],IActiveDesktop interface, IActiveDesktop interface [Legacy Windows Environment Features],GetDesktopItemByID method, IActiveDesktop.GetDesktopItemByID, IActiveDesktop::GetDesktopItemByID, _win32_IActiveDesktop_GetDesktopItemByID, lwef.iactivedesktop_getdesktopitembyid, shell.iactivedesktop_getdesktopitembyid, shlobj_core/IActiveDesktop::GetDesktopItemByID
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
 - IActiveDesktop.GetDesktopItemByID
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IActiveDesktop::GetDesktopItemByID


## -description


Gets the desktop item that matches the given identification.


## -parameters




### -param dwID

Type: <b>ULONG_PTR</b>

An unsigned long integer value that contains the desktop item's identification. 


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



The desktop item's identification is returned in the <b>dwID</b> member of the <a href="https://msdn.microsoft.com/2692a2d6-1d33-410f-987c-8388c636cae6">COMPONENT</a> structure that is returned from the <a href="https://msdn.microsoft.com/b9d4a771-023f-4a31-b9b7-39b8b4a8695a">IActiveDesktop::GetDesktopItem</a> method. This identification is only valid until the <a href="https://msdn.microsoft.com/3bac5af5-f4a6-4822-83de-11633beef88a">IActiveDesktop::ApplyChanges</a> method is called. Applications that must retrieve the same desktop item consistently should enumerate the desktop items using the <b>IActiveDesktop::GetDesktopItem</b> and <a href="https://msdn.microsoft.com/d2bba6f8-4ff0-4978-93ae-46db9ec6ea48">IActiveDesktop::GetDesktopItemCount</a> methods. 




## -see-also




<a href="https://msdn.microsoft.com/4d572b86-36e8-417b-857c-eb477c04c691">IActiveDesktop</a>
 

 

