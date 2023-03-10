---
UID: NF:commoncontrols.IImageList.GetIcon
title: IImageList::GetIcon (commoncontrols.h)
description: Creates an icon from an image and a mask in an image list.
helpviewer_keywords: ["GetIcon","GetIcon method [Windows Controls]","GetIcon method [Windows Controls]","IImageList interface","IImageList interface [Windows Controls]","GetIcon method","IImageList.GetIcon","IImageList::GetIcon","comctl_IImageList_GetIcon","comctl_IImageList_GetIcon_cpp","commoncontrols/IImageList::GetIcon","controls.IImageList_GetIcon","controls.comctl_IImageList_GetIcon"]
old-location: controls\IImageList_GetIcon.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\imagelist\ifaces\iimagelist\geticon.htm
ms.date: 12/05/2018
ms.keywords: GetIcon, GetIcon method [Windows Controls], GetIcon method [Windows Controls],IImageList interface, IImageList interface [Windows Controls],GetIcon method, IImageList.GetIcon, IImageList::GetIcon, comctl_IImageList_GetIcon, comctl_IImageList_GetIcon_cpp, commoncontrols/IImageList::GetIcon, controls.IImageList_GetIcon, controls.comctl_IImageList_GetIcon
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
 - IImageList::GetIcon
 - commoncontrols/IImageList::GetIcon
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
 - IImageList.GetIcon
---

# IImageList::GetIcon


## -description

Creates an icon from an image and a mask in an image list.

## -parameters

### -param i [in]

Type: <b>int</b>

A value of type <b>int</b> that contains the index of the image.

### -param flags [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

A combination of flags that specify the drawing style. For a list of values, see <a href="/windows/desktop/api/commoncontrols/nf-commoncontrols-iimagelist-draw">IImageList::Draw</a>.

### -param picon [out]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HICON</a>*</b>

A pointer to an <b>int</b> that contains the handle to the icon if successful, or <b>NULL</b> if otherwise.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The calling application must destroy the icon returned from this method using <a href="/windows/desktop/api/winuser/nf-winuser-destroyicon">DestroyIcon</a>. 
		

To use <b>IImageList::GetIcon</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="/windows/desktop/Controls/cookbook-overview">Enabling Visual Styles</a>.