---
UID: NF:commoncontrols.IImageList.GetDragImage
title: IImageList::GetDragImage
author: windows-sdk-content
description: Gets the temporary image list that is used for the drag image. The function also retrieves the current drag position and the offset of the drag image relative to the drag position.
old-location: controls\IImageList_GetDragImage.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\imagelist\ifaces\iimagelist\getdragimage.htm
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: GetDragImage, GetDragImage method [Windows Controls], GetDragImage method [Windows Controls],IImageList interface, IImageList interface [Windows Controls],GetDragImage method, IImageList.GetDragImage, IImageList::GetDragImage, comctl_IImageList_GetDragImage, comctl_IImageList_GetDragImage_cpp, commoncontrols/IImageList::GetDragImage, controls.IImageList_GetDragImage, controls.comctl_IImageList_GetDragImage
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
 - IImageList.GetDragImage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IImageList::GetDragImage


## -description


Gets the temporary image list that is used for the drag image. The function also retrieves the current drag position and the offset of the drag image relative to the drag position. 
		


## -parameters




### -param ppt [out]

Type: <b><a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a> structure that receives the current drag position. Can be <b>NULL</b>. 
				


### -param pptHotspot [out]

Type: <b><a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a> structure that receives the offset of the drag image relative to the drag position. Can be <b>NULL</b>.
				


### -param riid [out]

Type: <b>REFIID</b>

An IID for the image list.


### -param ppv [out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">PVOID</a>*</b>

The address of a pointer to the interface for the image list if successful, <b>NULL</b> otherwise.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The temporary image list is destroyed when <a href="https://msdn.microsoft.com/en-us/library/Bb761457(v=VS.85).aspx">IImageList::EndDrag</a> is called. To begin a drag operation, use <a href="https://msdn.microsoft.com/en-us/library/Bb761440(v=VS.85).aspx">IImageList::BeginDrag</a>. 		
		

To use <b>IImageList::GetDragImage</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="https://msdn.microsoft.com/en-us/library/Bb773175(v=VS.85).aspx">Enabling Visual Styles</a>. 



