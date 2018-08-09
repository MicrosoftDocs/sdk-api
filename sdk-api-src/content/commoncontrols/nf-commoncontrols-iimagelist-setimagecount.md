---
UID: NF:commoncontrols.IImageList.SetImageCount
title: IImageList::SetImageCount
author: windows-sdk-content
description: Resizes an existing image list.
old-location: controls\IImageList_SetImageCount.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\imagelist\ifaces\iimagelist\setimagecount.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IImageList interface [Windows Controls],SetImageCount method, IImageList.SetImageCount, IImageList::SetImageCount, SetImageCount, SetImageCount method [Windows Controls], SetImageCount method [Windows Controls],IImageList interface, comctl_IImageList_SetImageCount, comctl_IImageList_SetImageCount_cpp, commoncontrols/IImageList::SetImageCount, controls.IImageList_SetImageCount, controls.comctl_IImageList_SetImageCount
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
 - IImageList.SetImageCount
product: Windows
targetos: Windows
req.lib: 
req.dll: Comctl32.dll (version 6.0 or later)
req.irql: 
---

# IImageList::SetImageCount


## -description


Resizes an existing image list. 
		


## -parameters




### -param uNewCount [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

A value that specifies the new size of the image list. 
				


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If an application expands an image list using this method, it must add new images by using <a href="https://msdn.microsoft.com/1a8cd814-2b48-4ab4-9d7b-24c049c8e8fc">IImageList::Replace</a>. If the application does not add valid images to the new indexes, draw operations that use the new indexes are unpredictable. 
		

If you decrease the size of an image list using this method, images at the end of the list for which there is no longer room are truncated from the list.  Images truncated in this manner are automatically deallocated. 

To use <b>IImageList::SetImageCount</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="https://msdn.microsoft.com/eb6c2469-25b9-43c4-a6ca-391a7b2859b3">Enabling Visual Styles</a>. 



