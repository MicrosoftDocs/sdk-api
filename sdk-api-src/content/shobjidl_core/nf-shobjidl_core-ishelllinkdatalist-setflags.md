---
UID: NF:shobjidl_core.IShellLinkDataList.SetFlags
title: IShellLinkDataList::SetFlags
author: windows-driver-content
description: Sets the current option settings.
old-location: shell\IShellLinkDataList_SetFlags.htm
old-project: shell
ms.assetid: 0fca6394-e8ad-4ef3-a7d8-60e85229556b
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: IShellLinkDataList interface [Windows Shell],SetFlags method, IShellLinkDataList.SetFlags, IShellLinkDataList::SetFlags, SetFlags, SetFlags method [Windows Shell], SetFlags method [Windows Shell],IShellLinkDataList interface, _win32_IShellLinkDataList_SetFlags, shell.IShellLinkDataList_SetFlags, shobjidl_core/IShellLinkDataList::SetFlags
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Shell32.dll
api_name:
-	IShellLinkDataList.SetFlags
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
req.product: Outlook Express 6.0
---

# IShellLinkDataList::SetFlags


## -description


Sets the current option settings.


## -parameters




### -param dwFlags [in]

Type: <b>DWORD</b>

One or more of the <a href="https://msdn.microsoft.com/3b810223-b2d9-40ca-92bd-4d9f31981355">SHELL_LINK_DATA_FLAGS</a> that indicate the option settings.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/ac3279ad-1413-48bf-a830-4ec128352573">IShellLinkDataList</a>
 

 

