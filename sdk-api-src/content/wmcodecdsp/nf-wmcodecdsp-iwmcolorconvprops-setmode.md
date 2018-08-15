---
UID: NF:wmcodecdsp.IWMColorConvProps.SetMode
title: IWMColorConvProps::SetMode
author: windows-sdk-content
description: Specifies whether the input video stream is interlaced.
old-location: mf\iwmcolorconvpropssetmode.htm
old-project: medfound
ms.assetid: b0be2965-36cf-4d14-8df6-c5296135a8e5
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: IWMColorConvProps interface [Media Foundation],SetMode method, IWMColorConvProps.SetMode, IWMColorConvProps::SetMode, SetMode, SetMode method [Media Foundation], SetMode method [Media Foundation],IWMColorConvProps interface, codecapi.iwmcolorconvpropssetmode, mf.iwmcolorconvpropssetmode, wmcodecdsp/IWMColorConvProps::SetMode
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wmcodecdsp.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: MFVideoDSPMode
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmcodecdsp.h
api_name:
 - IWMColorConvProps.SetMode
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMColorConvProps::SetMode


## -description


Specifies whether the input video stream is interlaced.



## -parameters




### -param lMode [in]

Specifies one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Progressive video

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Interlaced video

</td>
</tr>
</table>
 


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



By default, the color converter uses the input media type to determine whether the video is interlaced. You can call this method to override the media type setting. 

This method is equivalent to setting the <a href="https://msdn.microsoft.com/d0d93151-5b0d-44a7-8497-f11b3e23a031">MFPKEY_COLORCONV_MODE</a> property.




## -see-also




<a href="https://msdn.microsoft.com/c4a6b7c1-edc0-4030-ac47-895580ad294d">IWMColorConvProps Interface</a>
 

 

