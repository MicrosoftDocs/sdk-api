---
UID: NF:commoncontrols.IImageList2.Resize
title: IImageList2::Resize
author: windows-sdk-content
description: Resizes the current image.
old-location: controls\IImageList2_Resize.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\imagelist\ifaces\iimagelist2\resize.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IImageList2 interface [Windows Controls],Resize method, IImageList2.Resize, IImageList2::Resize, Resize, Resize method [Windows Controls], Resize method [Windows Controls],IImageList2 interface, _shell_IImageList2_Resize, _shell_IImageList2_Resize_cpp, commoncontrols/IImageList2::Resize, controls.IImageList2_Resize, controls._shell_IImageList2_Resize
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: commoncontrols.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Commoncontrols.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: OFNOTIFYW, *LPOFNOTIFYW
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Comctl32.dll
api_name:
 - IImageList2.Resize
product: Windows
targetos: Windows
req.lib: 
req.dll: Comctl32.dll (version 6.0 or later)
req.irql: 
---

# IImageList2::Resize


## -description


Resizes the current image.


## -parameters




### -param cxNewIconSize [in]

Type: <b>int</b>

The x-axis count, in pixels, for the new size.


### -param cyNewIconSize [in]

Type: <b>int</b>

The y-axis count, in pixels, for the new size.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



