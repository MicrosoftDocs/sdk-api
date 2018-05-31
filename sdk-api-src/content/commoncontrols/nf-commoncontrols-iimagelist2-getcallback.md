---
UID: NF:commoncontrols.IImageList2.GetCallback
title: IImageList2::GetCallback
author: windows-sdk-content
description: Gets an image list callback object.
old-location: controls\IImageList2_GetCallback.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\imagelist\ifaces\iimagelist2\getcallback.htm
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: GetCallback, GetCallback method [Windows Controls], GetCallback method [Windows Controls],IImageList2 interface, IImageList2 interface [Windows Controls],GetCallback method, IImageList2.GetCallback, IImageList2::GetCallback, _shell_IImageList2_GetCallback, _shell_IImageList2_GetCallback_cpp, commoncontrols/IImageList2::GetCallback, controls.IImageList2_GetCallback, controls._shell_IImageList2_GetCallback
ms.prod: windows
ms.technology: windows-sdk
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
-	IImageList2.GetCallback
product: Windows
targetos: Windows
req.lib: 
req.dll: Comctl32.dll (version 6.0 or later)
req.irql: 
---

# IImageList2::GetCallback


## -description


Gets an image list callback object.


## -parameters




### -param riid [in]

Type: <b>REFIID</b>

Reference to a desired IID.


### -param ppv [out]

Type: <b>void**</b>

Contains the address of a pointer to a callback object.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



