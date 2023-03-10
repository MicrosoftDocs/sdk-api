---
UID: NF:commoncontrols.IImageList2.Resize
title: IImageList2::Resize (commoncontrols.h)
description: Resizes the current image.
helpviewer_keywords: ["IImageList2 interface [Windows Controls]","Resize method","IImageList2.Resize","IImageList2::Resize","Resize","Resize method [Windows Controls]","Resize method [Windows Controls]","IImageList2 interface","_shell_IImageList2_Resize","_shell_IImageList2_Resize_cpp","commoncontrols/IImageList2::Resize","controls.IImageList2_Resize","controls._shell_IImageList2_Resize"]
old-location: controls\IImageList2_Resize.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\imagelist\ifaces\iimagelist2\resize.htm
ms.date: 12/05/2018
ms.keywords: IImageList2 interface [Windows Controls],Resize method, IImageList2.Resize, IImageList2::Resize, Resize, Resize method [Windows Controls], Resize method [Windows Controls],IImageList2 interface, _shell_IImageList2_Resize, _shell_IImageList2_Resize_cpp, commoncontrols/IImageList2::Resize, controls.IImageList2_Resize, controls._shell_IImageList2_Resize
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
 - IImageList2::Resize
 - commoncontrols/IImageList2::Resize
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
 - IImageList2.Resize
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

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.