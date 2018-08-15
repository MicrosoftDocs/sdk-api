---
UID: NE:wincodec.WICGifImageDescriptorProperties
title: WICGifImageDescriptorProperties
author: windows-sdk-content
description: Specifies the image descriptor metadata properties for Graphics Interchange Format (GIF) frames.
old-location: wic\_wic_codec_wicgifimagedescriptorproperties.htm
old-project: wic
ms.assetid: 5488e63b-503b-47cd-99f3-5d359c7e0070
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: WICGifImageDescriptorHeight, WICGifImageDescriptorInterlaceFlag, WICGifImageDescriptorLeft, WICGifImageDescriptorLocalColorTableFlag, WICGifImageDescriptorLocalColorTableSize, WICGifImageDescriptorProperties, WICGifImageDescriptorProperties enumeration [Windows Imaging Component], WICGifImageDescriptorSortFlag, WICGifImageDescriptorTop, WICGifImageDescriptorWidth, _wic_codec_wicgifimagedescriptorproperties, wic._wic_codec_wicgifimagedescriptorproperties, wincodec/WICGifImageDescriptorHeight, wincodec/WICGifImageDescriptorInterlaceFlag, wincodec/WICGifImageDescriptorLeft, wincodec/WICGifImageDescriptorLocalColorTableFlag, wincodec/WICGifImageDescriptorLocalColorTableSize, wincodec/WICGifImageDescriptorProperties, wincodec/WICGifImageDescriptorSortFlag, wincodec/WICGifImageDescriptorTop, wincodec/WICGifImageDescriptorWidth
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: wincodec.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodec.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WICGifImageDescriptorProperties
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincodec.h
api_name:
 - WICGifImageDescriptorProperties
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# WICGifImageDescriptorProperties enumeration


## -description


Specifies the image descriptor metadata properties for  Graphics Interchange Format (GIF) frames.


## -enum-fields




### -field WICGifImageDescriptorLeft

[VT_UI2] Indicates the X offset at which to locate this frame within the logical screen.


### -field WICGifImageDescriptorTop

[VT_UI2] Indicates the Y offset at which to locate this frame within the logical screen.


### -field WICGifImageDescriptorWidth

[VT_UI2] Indicates width of this frame, in pixels.


### -field WICGifImageDescriptorHeight

[VT_UI2] Indicates height of this frame, in pixels.


### -field WICGifImageDescriptorLocalColorTableFlag

[VT_BOOL] Indicates the local color table flag. <b>TRUE</b> if global color table is present; otherwise, <b>FALSE</b>.


### -field WICGifImageDescriptorInterlaceFlag

[VT_BOOL] Indicates the interlace flag. <b>TRUE</b> if image is interlaced; otherwise, <b>FALSE</b>.


### -field WICGifImageDescriptorSortFlag

[VT_BOOL] Indicates the sorted color table flag. <b>TRUE</b> if the color table is sorted from most frequently to least frequently used color; otherwise, <b>FALSE</b>.


### -field WICGifImageDescriptorLocalColorTableSize

[VT_UI1] Indicates the value used to calculate the number of bytes contained in the global color table. 

To calculate the actual size of the color table, raise 2 to the value of the field + 1.


### -field WICGifImageDescriptorProperties_FORCE_DWORD



