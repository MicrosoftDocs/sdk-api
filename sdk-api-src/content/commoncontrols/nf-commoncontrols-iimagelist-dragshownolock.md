---
UID: NF:commoncontrols.IImageList.DragShowNolock
title: IImageList::DragShowNolock
author: windows-sdk-content
description: Shows or hides the image being dragged.
old-location: controls\IImageList_DragShowNolock.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\imagelist\ifaces\iimagelist\dragshownolock.htm
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: DragShowNolock, DragShowNolock method [Windows Controls], DragShowNolock method [Windows Controls],IImageList interface, IImageList interface [Windows Controls],DragShowNolock method, IImageList.DragShowNolock, IImageList::DragShowNolock, comctl_IImageList_DragShowNolock, comctl_IImageList_DragShowNolock_cpp, commoncontrols/IImageList::DragShowNolock, controls.IImageList_DragShowNolock, controls.comctl_IImageList_DragShowNolock
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: Comctl32.dll (version 6.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Comctl32.dll
api_name:
 - IImageList.DragShowNolock
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IImageList::DragShowNolock


## -description


Shows or hides the image being dragged. 
		


## -parameters




### -param fShow [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

A value that specifies whether to show or hide the image being dragged. Specify <b>TRUE</b> to show the image or <b>FALSE</b> to hide the image. 
				


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To use <b>IImageList::DragShowNolock</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="https://msdn.microsoft.com/eb6c2469-25b9-43c4-a6ca-391a7b2859b3">Enabling Visual Styles</a>. 



