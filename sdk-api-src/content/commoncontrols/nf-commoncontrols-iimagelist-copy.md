---
UID: NF:commoncontrols.IImageList.Copy
title: IImageList::Copy (commoncontrols.h)
description: Copies images from a given image list.
helpviewer_keywords: ["Copy","Copy method [Windows Controls]","Copy method [Windows Controls]","IImageList interface","IImageList interface [Windows Controls]","Copy method","IImageList.Copy","IImageList::Copy","comctl_IImageList_Copy","comctl_IImageList_Copy_cpp","commoncontrols/IImageList::Copy","controls.IImageList_Copy","controls.comctl_IImageList_Copy"]
old-location: controls\IImageList_Copy.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\imagelist\ifaces\iimagelist\copy.htm
ms.date: 12/05/2018
ms.keywords: Copy, Copy method [Windows Controls], Copy method [Windows Controls],IImageList interface, IImageList interface [Windows Controls],Copy method, IImageList.Copy, IImageList::Copy, comctl_IImageList_Copy, comctl_IImageList_Copy_cpp, commoncontrols/IImageList::Copy, controls.IImageList_Copy, controls.comctl_IImageList_Copy
req.header: commoncontrols.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: CommonControls.idl
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
 - IImageList::Copy
 - commoncontrols/IImageList::Copy
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
 - IImageList.Copy
---

# IImageList::Copy


## -description

Copies images from a given image list.

## -parameters

### -param iDst [in]

Type: <b>int</b>

A value of type <b>int</b> that contains the zero-based index of the destination image for the copy operation.

### -param punkSrc [in]

Type: <b><a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>*</b>

A pointer to the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface for the source image list.

### -param iSrc [in]

Type: <b>int</b>

A value of type <b>int</b> that contains the zero-based index of the source image for the copy operation.

### -param uFlags [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

A value that specifies the type of copy operation to be made.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The <i>uFlags</i> parameter can have the following values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td><b>ILCF_MOVE</b></td>
<td>The source image is copied to the destination image's index. This operation results in multiple instances of a given image.
				</td>
</tr>
<tr>
<td><b>ILCF_SWAP</b></td>
<td>The source and destination images exchange positions within the image list.
				</td>
</tr>
</table>
 

To use <b>IImageList::Copy</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="/windows/desktop/Controls/cookbook-overview">Enabling Visual Styles</a>.