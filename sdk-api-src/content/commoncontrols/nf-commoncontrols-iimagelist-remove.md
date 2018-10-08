---
UID: NF:commoncontrols.IImageList.Remove
title: IImageList::Remove
author: windows-sdk-content
description: Removes an image from an image list.
old-location: controls\IImageList_Remove.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\imagelist\ifaces\iimagelist\remove.htm
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: IImageList interface [Windows Controls],Remove method, IImageList.Remove, IImageList::Remove, Remove, Remove method [Windows Controls], Remove method [Windows Controls],IImageList interface, comctl_IImageList_Remove, comctl_IImageList_Remove_cpp, commoncontrols/IImageList::Remove, controls.IImageList_Remove, controls.comctl_IImageList_Remove
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IImageList.Remove
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IImageList::Remove


## -description


Removes an image from an image list. 
		


## -parameters




### -param i [in]

Type: <b>int</b>

A value of type <b>int</b>  that contains the index of the image to remove. If this parameter is -1, the method removes all images.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



When an image is removed, the indexes of the remaining images adjust so that they  always range from zero to one less than the number of images in the image list. For example, if you remove the image at index 0, then image 1 becomes image 0, image 2 becomes image 1, and so on. 
		

To use <b>IImageList::Remove</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="https://msdn.microsoft.com/en-us/library/Bb773175(v=VS.85).aspx">Enabling Visual Styles</a>. 



