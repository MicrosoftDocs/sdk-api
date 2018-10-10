---
UID: NF:commoncontrols.IImageList2.ReplaceFromImageList
title: IImageList2::ReplaceFromImageList
author: windows-sdk-content
description: Replaces an image in one image list with an image from another image list.
old-location: controls\IImageList2_ReplaceFromImageList.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\imagelist\ifaces\iimagelist2\replacefromimagelist.htm
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: IImageList2 interface [Windows Controls],ReplaceFromImageList method, IImageList2.ReplaceFromImageList, IImageList2::ReplaceFromImageList, ReplaceFromImageList, ReplaceFromImageList method [Windows Controls], ReplaceFromImageList method [Windows Controls],IImageList2 interface, _shell_IImageList2_ReplaceFromImageList, _shell_IImageList2_ReplaceFromImageList_cpp, commoncontrols/IImageList2::ReplaceFromImageList, controls.IImageList2_ReplaceFromImageList, controls._shell_IImageList2_ReplaceFromImageList
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Comctl32.dll
api_name:
 - IImageList2.ReplaceFromImageList
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IImageList2::ReplaceFromImageList


## -description


Replaces an image in one image list with an image from another image list.


## -parameters




### -param i [in]

Type: <b>int</b>

The index of the destination image in the image list. This is the image that is overwritten by the new image.


### -param pil [in]

Type: <b><a href="https://msdn.microsoft.com/02e397a4-22fa-49fb-8103-376aa5ebc77a">IImageList</a>*</b>

A pointer to the source image list.


### -param iSrc [in]

Type: <b>int</b>

The index of the source image in the image list pointed to by <i>pil</i>.


### -param punk [in, optional]

Type: <b><a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface.


### -param dwFlags [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Not used; must be 0.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



