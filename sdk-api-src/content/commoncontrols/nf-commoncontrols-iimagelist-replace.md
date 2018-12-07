---
UID: NF:commoncontrols.IImageList.Replace
title: IImageList::Replace
author: windows-sdk-content
description: Replaces an image in an image list with a new image.
old-location: controls\IImageList_Replace.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\imagelist\ifaces\iimagelist\replace.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IImageList interface [Windows Controls],Replace method, IImageList.Replace, IImageList::Replace, Replace, Replace method [Windows Controls], Replace method [Windows Controls],IImageList interface, comctl_IImageList_Replace, comctl_IImageList_Replace_cpp, commoncontrols/IImageList::Replace, controls.IImageList_Replace, controls.comctl_IImageList_Replace
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
req.idl: CommonControls.idl
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
 - IImageList.Replace
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IImageList::Replace


## -description


Replaces an image in an image list with a new image.


## -parameters




### -param i [in]

Type: <b>int</b>

A value of type <b>int</b> that contains the index of the image to replace.


### -param hbmImage [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HBITMAP</a></b>

A handle to the bitmap that contains the image.


### -param hbmMask [in, optional]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HBITMAP</a></b>

A handle to the bitmap that contains the mask. If no mask is used with the image list, this parameter is ignored.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<b>IImageList::Replace</b> copies the bitmap to an internal data structure. You must use <a href="https://msdn.microsoft.com/cc679af0-6839-4c83-9c42-39d7ededda40">DeleteObject</a> to delete <i>hbmImage</i> and <i>hbmMask</i> after the method returns.

To use <b>IImageList::Replace</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="https://msdn.microsoft.com/en-us/library/Bb773175(v=VS.85).aspx">Enabling Visual Styles</a>. 



