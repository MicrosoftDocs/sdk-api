---
UID: NF:commoncontrols.IImageList2.SetOriginalSize
title: IImageList2::SetOriginalSize (commoncontrols.h)
description: Sets the original size of a specified image.
helpviewer_keywords: ["IImageList2 interface [Windows Controls]","SetOriginalSize method","IImageList2.SetOriginalSize","IImageList2::SetOriginalSize","SetOriginalSize","SetOriginalSize method [Windows Controls]","SetOriginalSize method [Windows Controls]","IImageList2 interface","_shell_IImageList2_SetOriginalSize","_shell_IImageList2_SetOriginalSize_cpp","commoncontrols/IImageList2::SetOriginalSize","controls.IImageList2_SetOriginalSize","controls._shell_IImageList2_SetOriginalSize"]
old-location: controls\IImageList2_SetOriginalSize.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\imagelist\ifaces\iimagelist2\setoriginalsize.htm
ms.date: 12/05/2018
ms.keywords: IImageList2 interface [Windows Controls],SetOriginalSize method, IImageList2.SetOriginalSize, IImageList2::SetOriginalSize, SetOriginalSize, SetOriginalSize method [Windows Controls], SetOriginalSize method [Windows Controls],IImageList2 interface, _shell_IImageList2_SetOriginalSize, _shell_IImageList2_SetOriginalSize_cpp, commoncontrols/IImageList2::SetOriginalSize, controls.IImageList2_SetOriginalSize, controls._shell_IImageList2_SetOriginalSize
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
 - IImageList2::SetOriginalSize
 - commoncontrols/IImageList2::SetOriginalSize
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
 - IImageList2.SetOriginalSize
---

# IImageList2::SetOriginalSize


## -description

Sets the original size of a specified image.

## -parameters

### -param iImage [in]

Type: <b>int</b>

An index of desired image.

### -param cx [in]

Type: <b>int</b>

The x-axis count.

### -param cy [in]

Type: <b>int</b>

The y-axis count.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.