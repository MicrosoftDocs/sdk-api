---
UID: NF:commoncontrols.IImageList.ReplaceIcon
title: IImageList::ReplaceIcon (commoncontrols.h)
description: Replaces an image with an icon or cursor. (IImageList.ReplaceIcon)
helpviewer_keywords: ["IImageList interface [Windows Controls]","ReplaceIcon method","IImageList.ReplaceIcon","IImageList::ReplaceIcon","ReplaceIcon","ReplaceIcon method [Windows Controls]","ReplaceIcon method [Windows Controls]","IImageList interface","comctl_IImageList_ReplaceIcon","comctl_IImageList_ReplaceIcon_cpp","commoncontrols/IImageList::ReplaceIcon","controls.IImageList_ReplaceIcon","controls.comctl_IImageList_ReplaceIcon"]
old-location: controls\IImageList_ReplaceIcon.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\imagelist\ifaces\iimagelist\replaceicon.htm
ms.date: 12/05/2018
ms.keywords: IImageList interface [Windows Controls],ReplaceIcon method, IImageList.ReplaceIcon, IImageList::ReplaceIcon, ReplaceIcon, ReplaceIcon method [Windows Controls], ReplaceIcon method [Windows Controls],IImageList interface, comctl_IImageList_ReplaceIcon, comctl_IImageList_ReplaceIcon_cpp, commoncontrols/IImageList::ReplaceIcon, controls.IImageList_ReplaceIcon, controls.comctl_IImageList_ReplaceIcon
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
 - IImageList::ReplaceIcon
 - commoncontrols/IImageList::ReplaceIcon
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
 - IImageList.ReplaceIcon
---

# IImageList::ReplaceIcon


## -description

Replaces an image with an icon or cursor.

## -parameters

### -param i [in]

Type: <b>int</b>

A value of type <b>int</b> that contains the index of the image to replace. If i is -1, the function adds the image to the end of the list.

### -param hicon [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HICON</a></b>

A handle to the icon or cursor that contains the bitmap and mask for the new image.

### -param pi [out]

Type: <b>int*</b>

A pointer to an <b>int</b> that will contain the index of the image on return if 	successful, or -1 otherwise.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Because the system does not save <i>hicon</i>, you can destroy it after the function returns if the icon or cursor was created by <a href="/windows/desktop/api/winuser/nf-winuser-createicon">CreateIcon</a>. You do not need to destroy <i>hicon</i> if it was loaded by the <a href="/windows/desktop/api/winuser/nf-winuser-loadicona">LoadIcon</a> function; the system automatically frees an icon resource when it is no longer needed. 		
		

To use <b>IImageList::ReplaceIcon</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="/windows/desktop/Controls/cookbook-overview">Enabling Visual Styles</a>.
