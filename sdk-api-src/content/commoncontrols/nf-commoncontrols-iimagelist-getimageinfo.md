---
UID: NF:commoncontrols.IImageList.GetImageInfo
title: IImageList::GetImageInfo
author: windows-sdk-content
description: Gets information about an image.
old-location: controls\IImageList_GetImageInfo.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\imagelist\ifaces\iimagelist\getimageinfo.htm
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: GetImageInfo, GetImageInfo method [Windows Controls], GetImageInfo method [Windows Controls],IImageList interface, IImageList interface [Windows Controls],GetImageInfo method, IImageList.GetImageInfo, IImageList::GetImageInfo, comctl_IImageList_GetImageInfo, comctl_IImageList_GetImageInfo_cpp, commoncontrols/IImageList::GetImageInfo, controls.IImageList_GetImageInfo, controls.comctl_IImageList_GetImageInfo
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
 - IImageList.GetImageInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- commoncontrols.h
: 
- IImageList.GetImageInfo
: 
---

# IImageList::GetImageInfo


## -description


Gets information about an image. 
		


## -parameters




### -param i [in]

Type: <b>int</b>

A value of type <b>int</b> that contains the index of the image. 
				


### -param pImageInfo [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb761393(v=VS.85).aspx">IMAGEINFO</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/en-us/library/Bb761393(v=VS.85).aspx">IMAGEINFO</a> structure that receives information about the image. The information in this structure can directly manipulate the bitmaps of the image.
        


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To use <b>IImageList::GetImageInfo</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="https://msdn.microsoft.com/en-us/library/Bb773175(v=VS.85).aspx">Enabling Visual Styles</a>.
      



