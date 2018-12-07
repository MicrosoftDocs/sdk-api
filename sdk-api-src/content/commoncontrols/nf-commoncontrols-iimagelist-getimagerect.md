---
UID: NF:commoncontrols.IImageList.GetImageRect
title: IImageList::GetImageRect
author: windows-sdk-content
description: Gets an image's bounding rectangle.
old-location: controls\IImageList_GetImageRect.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\imagelist\ifaces\iimagelist\getimagerect.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetImageRect, GetImageRect method [Windows Controls], GetImageRect method [Windows Controls],IImageList interface, IImageList interface [Windows Controls],GetImageRect method, IImageList.GetImageRect, IImageList::GetImageRect, comctl_IImageList_GetImageRect, comctl_IImageList_GetImageRect_cpp, commoncontrols/IImageList::GetImageRect, controls.IImageList_GetImageRect, controls.comctl_IImageList_GetImageRect
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
 - IImageList.GetImageRect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IImageList::GetImageRect


## -description


Gets an image's bounding rectangle.
		


## -parameters




### -param i [in]

Type: <b>int</b>

A value of type <b>int</b> that contains the index of the image.


### -param prc [out]

Type: <b><a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a>*</b>

A pointer to a <b> RECT</b> that contains the bounding rectangle when the method returns.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To use <b>IImageList::GetImageRect</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="https://msdn.microsoft.com/en-us/library/Bb773175(v=VS.85).aspx">Enabling Visual Styles</a>. 



