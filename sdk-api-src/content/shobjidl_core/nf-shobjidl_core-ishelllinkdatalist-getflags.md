---
UID: NF:shobjidl_core.IShellLinkDataList.GetFlags
title: IShellLinkDataList::GetFlags (shobjidl_core.h)
author: windows-sdk-content
description: Gets the current option settings.
old-location: shell\IShellLinkDataList_GetFlags.htm
tech.root: shell
ms.assetid: d6ebfd84-6ef4-43be-af16-71fc395c4735
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetFlags, GetFlags method [Windows Shell], GetFlags method [Windows Shell],IShellLinkDataList interface, IShellLinkDataList interface [Windows Shell],GetFlags method, IShellLinkDataList.GetFlags, IShellLinkDataList::GetFlags, _win32_IShellLinkDataList_GetFlags, shell.IShellLinkDataList_GetFlags, shobjidl_core/IShellLinkDataList::GetFlags
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
req.lib: 
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IShellLinkDataList.GetFlags
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IShellLinkDataList::GetFlags


## -description


Gets the current option settings.


## -parameters




### -param pdwFlags [out]

Type: <b>DWORD*</b>

Pointer to one or more of the <a href="https://msdn.microsoft.com/3b810223-b2d9-40ca-92bd-4d9f31981355">SHELL_LINK_DATA_FLAGS</a> that indicate the current option settings.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/ac3279ad-1413-48bf-a830-4ec128352573">IShellLinkDataList</a>
 

 

