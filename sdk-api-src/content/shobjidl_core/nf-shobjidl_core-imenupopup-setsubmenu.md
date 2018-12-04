---
UID: NF:shobjidl_core.IMenuPopup.SetSubMenu
title: IMenuPopup::SetSubMenu
author: windows-sdk-content
description: Sets the given menu bar interface to be the submenu of the calling application object's interface.
old-location: shell\IMenuPopup_SetSubMenu.htm
tech.root: shell
ms.assetid: c2f80502-bac5-4a6f-95ba-1610c548e636
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: IMenuPopup interface [Windows Shell],SetSubMenu method, IMenuPopup.SetSubMenu, IMenuPopup::SetSubMenu, SetSubMenu, SetSubMenu method [Windows Shell], SetSubMenu method [Windows Shell],IMenuPopup interface, _win32_IMenuPopup_SetSubMenu, shell.IMenuPopup_SetSubMenu, shobjidl_core/IMenuPopup::SetSubMenu
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IMenuPopup.SetSubMenu
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMenuPopup::SetSubMenu


## -description


Sets the given menu bar interface to be the submenu of the calling application object's interface.


## -parameters




### -param pmp [in]

Type: <b><a href="https://msdn.microsoft.com/dc5749b1-43b7-4f68-ac38-8a6e99613149">IMenuPopup</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/dc5749b1-43b7-4f68-ac38-8a6e99613149">IMenuPopup</a> interface that specifies the menu bar of interest.


### -param fSet

Type: <b>BOOL</b>

Removes the submenu if <i>fSet</i> is set to <b>FALSE</b>.


## -returns



Type: <b>HRESULT</b>

Always returns S_OK.



