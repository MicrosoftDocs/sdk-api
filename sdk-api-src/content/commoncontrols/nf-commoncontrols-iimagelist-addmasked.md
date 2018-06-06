---
UID: NF:commoncontrols.IImageList.AddMasked
title: IImageList::AddMasked
author: windows-sdk-content
description: Adds an image or images to an image list, generating a mask from the specified bitmap.
old-location: controls\IImageList_AddMasked.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\imagelist\ifaces\iimagelist\addmasked.htm
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: AddMasked, AddMasked method [Windows Controls], AddMasked method [Windows Controls],IImageList interface, IImageList interface [Windows Controls],AddMasked method, IImageList.AddMasked, IImageList::AddMasked, comctl_IImageList_AddMasked, comctl_IImageList_AddMasked_cpp, commoncontrols/IImageList::AddMasked, controls.IImageList_AddMasked, controls.comctl_IImageList_AddMasked
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: OFNOTIFYW, *LPOFNOTIFYW
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Comctl32.dll
api_name:
 - IImageList.AddMasked
product: Windows
targetos: Windows
req.lib: 
req.dll: Comctl32.dll (version 6.0 or later)
req.irql: 
---

# IImageList::AddMasked


## -description



		Adds an image or images to an image list, generating a mask from the specified bitmap. 
		


## -parameters




### -param hbmImage [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HBITMAP</a></b>

A handle to the bitmap that contains one or more images. The number of images is inferred from the width of the bitmap. 
				


### -param crMask [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">COLORREF</a></b>

The color used to generate the mask. Each pixel of this color in the specified bitmap is changed to black, and the corresponding bit in the mask is set to 1. 
				


### -param pi [out]

Type: <b>int*</b>

A pointer to an <b>int</b> that contains the index of the first new image when it returns, if successful, or -1 otherwise.
				


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<div class="alert"><b>Note</b>  The bitmap passed in <i>hbmImage</i> will be modified.</div>
<div> </div>
<b>IImageList::AddMasked</b> copies the bitmap to an internal data structure. Bitmaps with color depth greater than 8bpp are not supported. You must use the <a href="https://msdn.microsoft.com/cc679af0-6839-4c83-9c42-39d7ededda40">DeleteObject</a> function to delete <i>hbmImage</i> and <i>crMask</i> after the method returns. 
		

To use <b>IImageList::AddMasked</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="https://msdn.microsoft.com/eb6c2469-25b9-43c4-a6ca-391a7b2859b3">Enabling Visual Styles</a>. 



