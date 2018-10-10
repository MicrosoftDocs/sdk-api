---
UID: NS:commoncontrols.tagIMAGEINFO
title: tagIMAGEINFO
author: windows-sdk-content
description: Contains information about an image in an image list. This structure is used with the IImageList::GetImageInfo function.
old-location: controls\IMAGEINFO.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\imagelist\structures\imageinfo.htm
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: "*LPIMAGEINFO, IMAGEINFO, IMAGEINFO structure [Windows Controls], LPIMAGEINFO, LPIMAGEINFO structure pointer [Windows Controls], _win32_IMAGEINFO, _win32_IMAGEINFO_cpp, commoncontrols/IMAGEINFO, commoncontrols/LPIMAGEINFO, controls.IMAGEINFO, controls._win32_IMAGEINFO, tagIMAGEINFO"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: commoncontrols.h
req.include-header: Commctrl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - commoncontrols.h
api_name:
 - IMAGEINFO
product: Windows
targetos: Windows
req.typenames: IMAGEINFO
req.redist: 
---

# tagIMAGEINFO structure


## -description


Contains information about an image in an image list. This structure is used with the <a href="https://msdn.microsoft.com/en-us/library/Bb761482(v=VS.85).aspx">IImageList::GetImageInfo</a> function. 


## -struct-fields




### -field hbmImage

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HBITMAP</a></b>

A handle to the bitmap that contains the images. 


### -field hbmMask

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HBITMAP</a></b>

A handle to a monochrome bitmap that contains the masks for the images. If the image list does not contain a mask, this member is <b>NULL</b>. 


### -field Unused1

Type: <b>int</b>

Not used. This member should always be zero. 


### -field Unused2

Type: <b>int</b>

Not used. This member should always be zero. 


### -field rcImage

Type: <b><a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a></b>

The bounding rectangle of the specified image within the bitmap specified by 
					<b>hbmImage</b>. 

