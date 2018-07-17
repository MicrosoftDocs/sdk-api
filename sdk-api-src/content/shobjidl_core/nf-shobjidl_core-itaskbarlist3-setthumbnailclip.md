---
UID: NF:shobjidl_core.ITaskbarList3.SetThumbnailClip
title: ITaskbarList3::SetThumbnailClip
author: windows-sdk-content
description: Selects a portion of a window's client area to display as that window's thumbnail in the taskbar.
old-location: shell\ITaskbarList3_SetThumbnailClip.htm
old-project: shell
ms.assetid: a22c4708-af59-4ccb-9ddb-885d14c17a33
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: ITaskbarList3 interface [Windows Shell],SetThumbnailClip method, ITaskbarList3.SetThumbnailClip, ITaskbarList3::SetThumbnailClip, SetThumbnailClip, SetThumbnailClip method [Windows Shell], SetThumbnailClip method [Windows Shell],ITaskbarList3 interface, _shell_ITaskbarList3_SetThumbnailClip, shell.ITaskbarList3_SetThumbnailClip, shobjidl_core/ITaskbarList3::SetThumbnailClip
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Explorerframe.dll
api_name:
 - ITaskbarList3.SetThumbnailClip
product: Windows
targetos: Windows
req.lib: Explorerframe.lib
req.dll: Explorerframe.dll
req.irql: 
req.product: Outlook Express 6.0
---

# ITaskbarList3::SetThumbnailClip


## -description


Selects a portion of a window's client area to display as that window's thumbnail in the taskbar.


## -parameters




### -param hwnd [in]

Type: <b>HWND</b>

The handle to a window represented in the taskbar.


### -param prcClip [in]

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure that specifies a selection within the window's client area, relative to the upper-left corner of that client area. To clear a clip that is already in place and return to the default display of the thumbnail, set this parameter to <b>NULL</b>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/c63f5fe8-4a8f-4ca8-bd6a-7733110bbb38">ITaskbarList</a>



<a href="https://msdn.microsoft.com/8af23586-349f-4d21-98cb-0aaa27a586ff">ITaskbarList2</a>



<a href="https://msdn.microsoft.com/a5eb4e5a-df17-4aca-96fb-d8475e266b92">ITaskbarList3</a>



<a href="https://msdn.microsoft.com/cbf2b07d-d67c-4755-888c-d40692d13cae">Taskbar Extensions</a>
 

 

