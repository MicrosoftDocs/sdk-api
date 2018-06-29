---
UID: NF:commoncontrols.IImageList.Merge
title: IImageList::Merge
author: windows-sdk-content
description: Creates a new image by combining two existing images. This method also creates a new image list in which to store the image.
old-location: controls\IImageList_Merge.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\imagelist\ifaces\iimagelist\merge.htm
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: IImageList interface [Windows Controls],Merge method, IImageList.Merge, IImageList::Merge, Merge, Merge method [Windows Controls], Merge method [Windows Controls],IImageList interface, comctl_IImageList_Merge, comctl_IImageList_Merge_cpp, commoncontrols/IImageList::Merge, controls.IImageList_Merge, controls.comctl_IImageList_Merge
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
 - IImageList.Merge
product: Windows
targetos: Windows
req.lib: 
req.dll: Comctl32.dll (version 6.0 or later)
req.irql: 
---

# IImageList::Merge


## -description



		Creates a new image by combining two existing images. This method also creates a new image list in which to store the image. 
		


## -parameters




### -param i1 [in]

Type: <b>int</b>

A value of type <b>int</b> that contains the index of the first existing image. 
				


### -param punk2 [in]

Type: <b><a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface of the image list that contains the second image. 			


### -param i2 [in]

Type: <b>int</b>

A value of type <b>int</b> that contains the index of the second existing image. 
				


### -param dx [in]

Type: <b>int</b>

A value of type <b>int</b>  that contains the x-component of the offset of the second image relative to the first image. 
				


### -param dy [in]

Type: <b>int</b>

A value of type <b>int</b>  that contains the y-component of the offset of the second image relative to the first image. 
				


### -param riid [out]

Type: <b>REFIID</b>

An IID of the interface for the new image list.


### -param ppv [out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">PVOID</a>*</b>

A raw pointer to the interface for the new image list.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks




		The new image consists of the second image drawn transparently over the first. 	The mask for the new image is obtained by combining the masks of the two existing images with the bitwise OR operator.

To use <b>IImageList::Merge</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="https://msdn.microsoft.com/library/Bb773175(v=VS.85).aspx">Enabling Visual Styles</a>. 



