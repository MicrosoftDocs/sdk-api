---
UID: NF:shobjidl_core.IShellMenu.GetMenuInfo
title: IShellMenu::GetMenuInfo (shobjidl_core.h)
author: windows-sdk-content
description: Gets information from the IShellMenu::Initialize method.
old-location: shell\IShellMenu_GetMenuInfo.htm
tech.root: shell
ms.assetid: 979d43ce-d8e6-444f-8082-49b52c0ad2ef
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetMenuInfo, GetMenuInfo method [Windows Shell], GetMenuInfo method [Windows Shell],IShellMenu interface, IShellMenu interface [Windows Shell],GetMenuInfo method, IShellMenu.GetMenuInfo, IShellMenu::GetMenuInfo, _shell_IShellMenu_GetMenuInfo, shell.IShellMenu_GetMenuInfo, shobjidl_core/IShellMenu::GetMenuInfo
ms.topic: method
f1_keywords: 
 - "shobjidl_core/IShellMenu.GetMenuInfo"
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
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
req.dll: Shell32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IShellMenu.GetMenuInfo
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IShellMenu::GetMenuInfo


## -description


Gets information from the <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenu-initialize">IShellMenu::Initialize</a> method.


## -parameters




### -param ppsmc [out, optional]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellmenucallback">IShellMenuCallback</a>**</b>

When this method returns, contains the address of a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellmenucallback">IShellMenuCallback</a> interface that you specified when you called <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenu-initialize">IShellMenu::Initialize</a>. This pointer can be <b>NULL</b>.


### -param puId [out, optional]

Type: <b>UINT*</b>

When this method returns, contains a pointer to a <b>UINT</b> value that receives the <i>uID</i> value that you specified when you called <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenu-initialize">IShellMenu::Initialize</a>. This pointer can be <b>NULL</b>.


### -param puIdAncestor [out, optional]

Type: <b>UINT*</b>

When this method returns, contains a pointer to a <b>UINT</b> value that receives the <i>uIdAncestor</i> value that you specified when you called <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenu-initialize">IShellMenu::Initialize</a>. This pointer can be <b>NULL</b>.


### -param pdwFlags [out]

Type: <b>DWORD*</b>

When this method returns, contains a pointer to a <b>DWORD</b> value that receives the <i>dwFlags</i> value that you specified when you called <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenu-initialize">IShellMenu::Initialize</a>. This pointer can be <b>NULL</b>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



