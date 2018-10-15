---
UID: NF:commoncontrols.IImageList.ReplaceIcon
title: IImageList::ReplaceIcon
author: windows-sdk-content
description: Replaces an image with an icon or cursor.
old-location: controls\IImageList_ReplaceIcon.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\imagelist\ifaces\iimagelist\replaceicon.htm
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: IImageList interface [Windows Controls],ReplaceIcon method, IImageList.ReplaceIcon, IImageList::ReplaceIcon, ReplaceIcon, ReplaceIcon method [Windows Controls], ReplaceIcon method [Windows Controls],IImageList interface, comctl_IImageList_ReplaceIcon, comctl_IImageList_ReplaceIcon_cpp, commoncontrols/IImageList::ReplaceIcon, controls.IImageList_ReplaceIcon, controls.comctl_IImageList_ReplaceIcon
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
 - IImageList.ReplaceIcon
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IImageList::ReplaceIcon


## -description


Replaces an image with an icon or cursor. 
		


## -parameters




### -param i [in]

Type: <b>int</b>

A value of type <b>int</b> that contains the index of the image to replace. If i is -1, the function adds the image to the end of the list. 
				


### -param hicon [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HICON</a></b>

A handle to the icon or cursor that contains the bitmap and mask for the new image. 
				


### -param pi [out]

Type: <b>int*</b>

A pointer to an <b>int</b> that will contain the index of the image on return if 	successful, or -1 otherwise. 
				


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Because the system does not save <i>hicon</i>, you can destroy it after the function returns if the icon or cursor was created by <a href="https://msdn.microsoft.com/73497232-fb99-4b9c-9ccb-575a9a6ece56">CreateIcon</a>. You do not need to destroy <i>hicon</i> if it was loaded by the <a href="https://msdn.microsoft.com/3a8099f8-9db7-4ef8-838f-ca8f272df531">LoadIcon</a> function; the system automatically frees an icon resource when it is no longer needed. 		
		

To use <b>IImageList::ReplaceIcon</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="https://msdn.microsoft.com/eb6c2469-25b9-43c4-a6ca-391a7b2859b3">Enabling Visual Styles</a>. 



