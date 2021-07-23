---
UID: NF:commoncontrols.IImageList2.Initialize
title: IImageList2::Initialize (commoncontrols.h)
description: Initializes an image list.
helpviewer_keywords: ["IImageList2 interface [Windows Controls]","Initialize method","IImageList2.Initialize","IImageList2::Initialize","Initialize","Initialize method [Windows Controls]","Initialize method [Windows Controls]","IImageList2 interface","_shell_IImageList2_Initialize","_shell_IImageList2_Initialize_cpp","commoncontrols/IImageList2::Initialize","controls.IImageList2_Initialize","controls._shell_IImageList2_Initialize"]
old-location: controls\IImageList2_Initialize.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\imagelist\ifaces\iimagelist2\initialize.htm
ms.date: 12/05/2018
ms.keywords: IImageList2 interface [Windows Controls],Initialize method, IImageList2.Initialize, IImageList2::Initialize, Initialize, Initialize method [Windows Controls], Initialize method [Windows Controls],IImageList2 interface, _shell_IImageList2_Initialize, _shell_IImageList2_Initialize_cpp, commoncontrols/IImageList2::Initialize, controls.IImageList2_Initialize, controls._shell_IImageList2_Initialize
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
 - IImageList2::Initialize
 - commoncontrols/IImageList2::Initialize
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
 - IImageList2.Initialize
---

# IImageList2::Initialize


## -description

Initializes an image list.

## -parameters

### -param cx [in]

Type: <b>int</b>

Width, in pixels, of each image.

### -param cy [in]

Type: <b>int</b>

Height, in pixels, of each image.

### -param flags [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

A combination of <a href="/windows/desktop/Controls/ilc-constants">Image List Creation Flags</a>.

### -param cInitial [in]

Type: <b>int</b>

Number of images that the image list initially contains.

### -param cGrow [in]

Type: <b>int</b>

Number of new images that the image list can contain.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.