---
UID: NF:commoncontrols.IImageList2.SetCallback
title: IImageList2::SetCallback (commoncontrols.h)
description: Sets an image list callback.
helpviewer_keywords: ["IImageList2 interface [Windows Controls]","SetCallback method","IImageList2.SetCallback","IImageList2::SetCallback","SetCallback","SetCallback method [Windows Controls]","SetCallback method [Windows Controls]","IImageList2 interface","_shell_IImageList2_SetCallback","_shell_IImageList2_SetCallback_cpp","commoncontrols/IImageList2::SetCallback","controls.IImageList2_SetCallback","controls._shell_IImageList2_SetCallback"]
old-location: controls\IImageList2_SetCallback.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\imagelist\ifaces\iimagelist2\setcallback.htm
ms.date: 12/05/2018
ms.keywords: IImageList2 interface [Windows Controls],SetCallback method, IImageList2.SetCallback, IImageList2::SetCallback, SetCallback, SetCallback method [Windows Controls], SetCallback method [Windows Controls],IImageList2 interface, _shell_IImageList2_SetCallback, _shell_IImageList2_SetCallback_cpp, commoncontrols/IImageList2::SetCallback, controls.IImageList2_SetCallback, controls._shell_IImageList2_SetCallback
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
 - IImageList2::SetCallback
 - commoncontrols/IImageList2::SetCallback
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
 - IImageList2.SetCallback
---

# IImageList2::SetCallback


## -description

Sets an image list callback.

## -parameters

### -param punk [in, optional]

Type: <b><a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>*</b>

A pointer to the callback interface.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.