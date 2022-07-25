---
UID: NN:shobjidl_core.IExtractImage
title: IExtractImage (shobjidl_core.h)
description: Exposes methods that request a thumbnail image from a Shell folder.
helpviewer_keywords: ["IExtractImage","IExtractImage interface [Windows Shell]","IExtractImage interface [Windows Shell]","described","_win32_IExtractImage","shell.IExtractImage","shobjidl_core/IExtractImage"]
old-location: shell\IExtractImage.htm
tech.root: shell
ms.assetid: 28a13749-89e7-407e-89cb-95464859ce3e
ms.date: 12/05/2018
ms.keywords: IExtractImage, IExtractImage interface [Windows Shell], IExtractImage interface [Windows Shell],described, _win32_IExtractImage, shell.IExtractImage, shobjidl_core/IExtractImage
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll (version 4.70 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IExtractImage
 - shobjidl_core/IExtractImage
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IExtractImage
---

# IExtractImage interface


## -description

Exposes methods that request a thumbnail image from a Shell folder.

## -inheritance

The <b>IExtractImage</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IExtractImage</b> also has these types of members:

## -remarks

There are two steps in the process: First, use <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iextractimage-getlocation">GetLocation</a> to request the path description of an image and specify how the image should be rendered. Then, call <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iextractimage-extract">Extract</a> to extract the image.

If the object is free-threaded it must also expose an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-irunnabletask">IRunnableTask</a> interface so it can be stopped and started as needed. This feature can be particularly useful when extraction may be slow.

Implement <b>IExtractImage</b> if your namespace extension needs to provide thumbnail images to be displayed in a Shellview.

Use <b>IExtractImage</b> if you are implementing a view of namespace objects, and want to display thumbnail images. You can use a Shell folder's <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getuiobjectof">IShellFolder::GetUIObjectOf</a> method to bind to its <b>IExtractImage</b> interface.
