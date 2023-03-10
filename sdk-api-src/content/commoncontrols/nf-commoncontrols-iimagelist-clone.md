---
UID: NF:commoncontrols.IImageList.Clone
title: IImageList::Clone (commoncontrols.h)
description: Clones an existing image list.
helpviewer_keywords: ["Clone","Clone method [Windows Controls]","Clone method [Windows Controls]","IImageList interface","IImageList interface [Windows Controls]","Clone method","IImageList.Clone","IImageList::Clone","comctl_IImageList_Clone","comctl_IImageList_Clone_cpp","commoncontrols/IImageList::Clone","controls.IImageList_Clone","controls.comctl_IImageList_Clone"]
old-location: controls\IImageList_Clone.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\imagelist\ifaces\iimagelist\clone.htm
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [Windows Controls], Clone method [Windows Controls],IImageList interface, IImageList interface [Windows Controls],Clone method, IImageList.Clone, IImageList::Clone, comctl_IImageList_Clone, comctl_IImageList_Clone_cpp, commoncontrols/IImageList::Clone, controls.IImageList_Clone, controls.comctl_IImageList_Clone
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
 - IImageList::Clone
 - commoncontrols/IImageList::Clone
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
 - IImageList.Clone
---

# IImageList::Clone


## -description

Clones an existing image list.

## -parameters

### -param riid [in]

Type: <b>REFIID</b>

An IID for the new image list.

### -param ppv [out]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">PVOID</a>*</b>

The address of a  pointer to the interface for the new image list.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

To use <b>IImageList::Clone</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="/windows/desktop/Controls/cookbook-overview">Enabling Visual Styles</a>.