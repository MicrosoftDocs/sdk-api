---
UID: NF:commoncontrols.IImageList2.GetCallback
title: IImageList2::GetCallback (commoncontrols.h)
description: Gets an image list callback object.
helpviewer_keywords: ["GetCallback","GetCallback method [Windows Controls]","GetCallback method [Windows Controls]","IImageList2 interface","IImageList2 interface [Windows Controls]","GetCallback method","IImageList2.GetCallback","IImageList2::GetCallback","_shell_IImageList2_GetCallback","_shell_IImageList2_GetCallback_cpp","commoncontrols/IImageList2::GetCallback","controls.IImageList2_GetCallback","controls._shell_IImageList2_GetCallback"]
old-location: controls\IImageList2_GetCallback.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\imagelist\ifaces\iimagelist2\getcallback.htm
ms.date: 12/05/2018
ms.keywords: GetCallback, GetCallback method [Windows Controls], GetCallback method [Windows Controls],IImageList2 interface, IImageList2 interface [Windows Controls],GetCallback method, IImageList2.GetCallback, IImageList2::GetCallback, _shell_IImageList2_GetCallback, _shell_IImageList2_GetCallback_cpp, commoncontrols/IImageList2::GetCallback, controls.IImageList2_GetCallback, controls._shell_IImageList2_GetCallback
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
req.lib: 
req.dll: Comctl32.dll (version 6.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IImageList2::GetCallback
 - commoncontrols/IImageList2::GetCallback
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Comctl32.dll
api_name:
 - IImageList2.GetCallback
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

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.