---
UID: NF:commoncontrols.IImageList.DragLeave
title: IImageList::DragLeave
author: windows-sdk-content
description: Unlocks the specified window and hides the drag image, which enables the window to update.
old-location: controls\IImageList_DragLeave.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\imagelist\ifaces\iimagelist\dragleave.htm
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: DragLeave, DragLeave method [Windows Controls], DragLeave method [Windows Controls],IImageList interface, IImageList interface [Windows Controls],DragLeave method, IImageList.DragLeave, IImageList::DragLeave, comctl_IImageList_DragLeave, comctl_IImageList_DragLeave_cpp, commoncontrols/IImageList::DragLeave, controls.IImageList_DragLeave, controls.comctl_IImageList_DragLeave
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: commoncontrols.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: CommonControls.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: OFNOTIFYW, *LPOFNOTIFYW
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Comctl32.dll
api_name:
-	IImageList.DragLeave
product: Windows
targetos: Windows
req.lib: 
req.dll: Comctl32.dll (version 6.0 or later)
req.irql: 
---

# IImageList::DragLeave


## -description



		Unlocks the specified window and hides the drag image, which enables the window to update.
		


## -parameters




### -param hwndLock [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the window that contains the drag image. 
				


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To use <b>IImageList::DragLeave</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="https://msdn.microsoft.com/eb6c2469-25b9-43c4-a6ca-391a7b2859b3">Enabling Visual Styles</a>. 



