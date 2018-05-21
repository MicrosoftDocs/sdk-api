---
UID: NF:commoncontrols.IImageList2.SetCallback
title: IImageList2::SetCallback
author: windows-driver-content
description: Sets an image list callback.
old-location: controls\IImageList2_SetCallback.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\imagelist\ifaces\iimagelist2\setcallback.htm
ms.author: windowsdriverdev
ms.date: 5/17/2018
ms.keywords: IImageList2 interface [Windows Controls],SetCallback method, IImageList2.SetCallback, IImageList2::SetCallback, SetCallback, SetCallback method [Windows Controls], SetCallback method [Windows Controls],IImageList2 interface, _shell_IImageList2_SetCallback, _shell_IImageList2_SetCallback_cpp, commoncontrols/IImageList2::SetCallback, controls.IImageList2_SetCallback, controls._shell_IImageList2_SetCallback
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: commoncontrols.h
req.include-header: 
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
req.typenames: OFNOTIFYW, *LPOFNOTIFYW
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Comctl32.dll
api_name:
-	IImageList2.SetCallback
product: Windows
targetos: Windows
req.lib: 
req.dll: Comctl32.dll (version 6.0 or later)
req.irql: 
---

# IImageList2::SetCallback


## -description


Sets an image list callback.


## -parameters




### -param punk [in, optional]

Type: <b><a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>*</b>

A pointer to the callback interface.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



