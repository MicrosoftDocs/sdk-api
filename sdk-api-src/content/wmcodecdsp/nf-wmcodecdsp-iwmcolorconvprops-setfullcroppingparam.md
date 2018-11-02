---
UID: NF:wmcodecdsp.IWMColorConvProps.SetFullCroppingParam
title: IWMColorConvProps::SetFullCroppingParam
author: windows-sdk-content
description: Sets the source and destination rectangles.
old-location: mf\iwmcolorconvpropssetfullcroppingparam.htm
tech.root: medfound
ms.assetid: 73545bbb-6630-463d-ad58-d24937e3b546
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: IWMColorConvProps interface [Media Foundation],SetFullCroppingParam method, IWMColorConvProps.SetFullCroppingParam, IWMColorConvProps::SetFullCroppingParam, SetFullCroppingParam, SetFullCroppingParam method [Media Foundation], SetFullCroppingParam method [Media Foundation],IWMColorConvProps interface, codecapi.iwmcolorconvpropssetfullcroppingparam, mf.iwmcolorconvpropssetfullcroppingparam, wmcodecdsp/IWMColorConvProps::SetFullCroppingParam
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wmcodecdsp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
 - COM
api_location:
 - wmcodecdsp.h
api_name:
 - IWMColorConvProps.SetFullCroppingParam
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMColorConvProps::SetFullCroppingParam


## -description


Sets the source and destination rectangles. 



## -parameters




### -param lSrcCropLeft [in]

Specifies the left edge of the source rectangle, in pixels.


### -param lSrcCropTop [in]

Specifies the top edge of the source rectangle, in pixels.


### -param lDstCropLeft [in]

Specifies the left edge of the destination rectangle, in pixels.


### -param lDstCropTop [in]

Specifies the top edge of the destination rectangle, in pixels.


### -param lCropWidth [in]

Specifies the width of the source and destination rectangles, in pixels.


### -param lCropHeight [in]

Specifies the height of the source and destination rectangles, in pixels.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>
 




## -remarks



By default, the color converter copies the entire video frame. When you call this method, the color converter crops the video to the source rectangle and copies that portion to the destination rectangle. 

This method is equivalent to setting the following properties:

<ul>
<li>
<a href="https://msdn.microsoft.com/d5450ff9-085f-4345-87af-bf6c87931755">MFPKEY_COLORCONV_SRCLEFT</a>
</li>
<li>
<a href="https://msdn.microsoft.com/1dfd5557-3f3b-4d59-9df6-e73cb1157619">MFPKEY_COLORCONV_SRCTOP</a>
</li>
<li>
<a href="https://msdn.microsoft.com/9411a7f7-0ce6-43b7-b50d-54489a7bb864">MFPKEY_COLORCONV_DSTLEFT</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e3ccbb23-0be3-4316-9e5f-0094fdb9e2db">MFPKEY_COLORCONV_DSTTOP</a>
</li>
<li>
<a href="https://msdn.microsoft.com/823f5fdf-a42c-47c0-aab4-3f43afd29c2b">MFPKEY_COLORCONV_WIDTH</a>
</li>
<li>
<a href="https://msdn.microsoft.com/be53d72f-f7b4-44a7-9231-fe0480daf49c">MFPKEY_COLORCONV_HEIGHT</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/c4a6b7c1-edc0-4030-ac47-895580ad294d">IWMColorConvProps</a>
 

 

