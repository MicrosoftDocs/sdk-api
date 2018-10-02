---
UID: NF:shobjidl_core.IFolderView.GetSpacing
title: IFolderView::GetSpacing
author: windows-sdk-content
description: Gets a POINT structure containing the width (x) and height (y) dimensions, including the surrounding white space, of an item.
old-location: shell\IFolderView_GetSpacing.htm
tech.root: Shell
ms.assetid: 6ea81c40-773f-4f53-97c1-99619e46be48
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: GetSpacing, GetSpacing method [Windows Shell], GetSpacing method [Windows Shell],IFolderView interface, IFolderView interface [Windows Shell],GetSpacing method, IFolderView.GetSpacing, IFolderView::GetSpacing, _shell_IFolderView_GetSpacing, shell.IFolderView_GetSpacing, shobjidl_core/IFolderView::GetSpacing
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
 - IFolderView.GetSpacing
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFolderView::GetSpacing


## -description


Gets a <a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a> structure containing the width (x) and height (y) dimensions, including the surrounding white space, of an item.


## -parameters




### -param ppt [in, out]

Type: <b><a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a>*</b>

A pointer to an existing structure to be filled with the current sizing dimensions of the items in the folder's view.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



As an example, consider an icon measuring 75 pixels by 70 pixels, with its upper-left corner located at pixel (0,0). Note that this measurement includes both the visible graphic and its surrounding buffer area. <b>IFolderView::GetSpacing</b> would return a pointer to a POINT structure containing an x value of 75 and a y value of 70. If you were using this information to avoid overlap, the next icon in line to the right would be placed with its upper-left corner at pixel (75,0). Similarly, the next icon below would be placed at pixel (0,70).




## -see-also




<a href="https://msdn.microsoft.com/3bc2615e-f07c-4959-b89e-bbbd2bf45a94">IFolderView</a>



<a href="https://msdn.microsoft.com/eb5f2dd6-1257-4cfc-a222-88e6c3b524ce">IFolderView::GetDefaultSpacing</a>
 

 

