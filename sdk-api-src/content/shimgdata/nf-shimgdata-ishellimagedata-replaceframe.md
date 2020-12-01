---
UID: NF:shimgdata.IShellImageData.ReplaceFrame
title: IShellImageData::ReplaceFrame (shimgdata.h)
description: Replaces the current frame with a new image.
helpviewer_keywords: ["IShellImageData interface [Windows Shell]","ReplaceFrame method","IShellImageData.ReplaceFrame","IShellImageData::ReplaceFrame","ReplaceFrame","ReplaceFrame method [Windows Shell]","ReplaceFrame method [Windows Shell]","IShellImageData interface","_shell_IShellImageData_ReplaceFrame","shell.IShellImageData_ReplaceFrame","shimgdata/IShellImageData::ReplaceFrame"]
old-location: shell\IShellImageData_ReplaceFrame.htm
tech.root: shell
ms.assetid: f066c503-4512-46db-be50-016996b92668
ms.date: 12/05/2018
ms.keywords: IShellImageData interface [Windows Shell],ReplaceFrame method, IShellImageData.ReplaceFrame, IShellImageData::ReplaceFrame, ReplaceFrame, ReplaceFrame method [Windows Shell], ReplaceFrame method [Windows Shell],IShellImageData interface, _shell_IShellImageData_ReplaceFrame, shell.IShellImageData_ReplaceFrame, shimgdata/IShellImageData::ReplaceFrame
req.header: shimgdata.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shimgdata.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IShellImageData::ReplaceFrame
 - shimgdata/IShellImageData::ReplaceFrame
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
 - IShellImageData.ReplaceFrame
---

# IShellImageData::ReplaceFrame


## -description

Replaces the current frame with a new image.

## -parameters

### -param pImg [in]

Type: <b>Image*</b>

The address of the new image.

## -returns

Type: <b>HRESULT</b>

Always returns S_OK.

## -remarks

You should also call <a href="/windows/desktop/api/shimgdata/nf-shimgdata-ishellimagedata-discardedit">IShellImageData::DiscardEdit</a> to ensure that any edited properties of the original image are not retained.

In the case of a multiframed image such as a .gif file, the current frame is replaced. In the case of non-multiframed images such a .jpg file, the entire image is replaced.

Replacing a frame in an animated .gif file causes that file's animation to no longer be functional. Replacing a frame in a Tagged Image File Format (TIFF) file could cause that file to lose pages, particularly if the TIFF frame's image is not the same size as the original. If possible, you should always replace a TIFF frame's image with a TIFF of the same size.

The <a href="/windows/desktop/api/shimgdata/nn-shimgdata-ishellimagedata">IShellImageData</a> implementation takes ownership of the image named in <i>pImg</i> and the caller should not try to use it after calling <b>IShellImageData::ReplaceFrame</b>.