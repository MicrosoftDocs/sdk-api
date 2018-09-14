---
UID: NF:shlobj_core.IActiveDesktop.SetDesktopItemOptions
title: IActiveDesktop::SetDesktopItemOptions
author: windows-sdk-content
description: Sets the item's options.
old-location: lwef\iactivedesktop_setdesktopitemoptions.htm
tech.root: lwef
ms.assetid: 5f2c1f41-d678-4eb8-b246-46133eec465f
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IActiveDesktop interface [Legacy Windows Environment Features],SetDesktopItemOptions method, IActiveDesktop.SetDesktopItemOptions, IActiveDesktop::SetDesktopItemOptions, SetDesktopItemOptions, SetDesktopItemOptions method [Legacy Windows Environment Features], SetDesktopItemOptions method [Legacy Windows Environment Features],IActiveDesktop interface, _win32_IActiveDesktop_SetDesktopItemOptions, lwef.iactivedesktop_setdesktopitemoptions, shell.iactivedesktop_setdesktopitemoptions, shlobj_core/IActiveDesktop::SetDesktopItemOptions
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
 - IActiveDesktop.SetDesktopItemOptions
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IActiveDesktop::SetDesktopItemOptions


## -description


Sets the item's options.


## -parameters




### -param pco

TBD


### -param dwReserved

Type: <b>DWORD</b>

Reserved. Must be set to zero. 


#### - pcomp [in]

Type: <b>LPCCOMPONENTSOPT</b>

The address of the <a href="https://msdn.microsoft.com/c56a2061-903a-4777-a3fc-bb1fae1f8c43">COMPONENTSOPT</a> structure that contains the options to set. 


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/4d572b86-36e8-417b-857c-eb477c04c691">IActiveDesktop</a>
 

 

