---
UID: NF:shobjidl_core.ITaskbarList3.SetThumbnailTooltip
title: ITaskbarList3::SetThumbnailTooltip
author: windows-sdk-content
description: Specifies or updates the text of the tooltip that is displayed when the mouse pointer rests on an individual preview thumbnail in a taskbar button flyout.
old-location: shell\ITaskbarList3_SetThumbnailTooltip.htm
tech.root: shell
ms.assetid: 73b5b9de-4876-4cac-9e58-d2e7559724f7
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: ITaskbarList3 interface [Windows Shell],SetThumbnailTooltip method, ITaskbarList3.SetThumbnailTooltip, ITaskbarList3::SetThumbnailTooltip, SetThumbnailTooltip, SetThumbnailTooltip method [Windows Shell], SetThumbnailTooltip method [Windows Shell],ITaskbarList3 interface, _shell_ITaskbarList3_SetThumbnailTooltip, shell.ITaskbarList3_SetThumbnailTooltip, shobjidl_core/ITaskbarList3::SetThumbnailTooltip
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: Explorerframe.lib
req.dll: Explorerframe.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Explorerframe.dll
api_name:
 - ITaskbarList3.SetThumbnailTooltip
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITaskbarList3::SetThumbnailTooltip


## -description


Specifies or updates the text of the tooltip that is displayed when the mouse pointer rests on an individual preview thumbnail in a taskbar button flyout.


## -parameters




### -param hwnd [in]

Type: <b>HWND</b>

The handle to the window whose thumbnail displays the tooltip. This handle must belong to the calling process.


### -param pszTip [in]

Type: <b>LPCWSTR</b>

The pointer to the text to be displayed in the tooltip. This value can be <b>NULL</b>, in which case the title of the window specified by <i>hwnd</i> is used as the tooltip.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/c63f5fe8-4a8f-4ca8-bd6a-7733110bbb38">ITaskbarList</a>



<a href="https://msdn.microsoft.com/8af23586-349f-4d21-98cb-0aaa27a586ff">ITaskbarList2</a>



<a href="https://msdn.microsoft.com/a5eb4e5a-df17-4aca-96fb-d8475e266b92">ITaskbarList3</a>



<a href="https://msdn.microsoft.com/cbf2b07d-d67c-4755-888c-d40692d13cae">Taskbar Extensions</a>
 

 

