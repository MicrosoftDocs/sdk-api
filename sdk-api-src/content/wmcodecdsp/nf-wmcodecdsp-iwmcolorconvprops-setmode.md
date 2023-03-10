---
UID: NF:wmcodecdsp.IWMColorConvProps.SetMode
title: IWMColorConvProps::SetMode (wmcodecdsp.h)
description: Specifies whether the input video stream is interlaced.
helpviewer_keywords: ["IWMColorConvProps interface [Media Foundation]","SetMode method","IWMColorConvProps.SetMode","IWMColorConvProps::SetMode","SetMode","SetMode method [Media Foundation]","SetMode method [Media Foundation]","IWMColorConvProps interface","codecapi.iwmcolorconvpropssetmode","mf.iwmcolorconvpropssetmode","wmcodecdsp/IWMColorConvProps::SetMode"]
old-location: mf\iwmcolorconvpropssetmode.htm
tech.root: mf
ms.assetid: b0be2965-36cf-4d14-8df6-c5296135a8e5
ms.date: 12/05/2018
ms.keywords: IWMColorConvProps interface [Media Foundation],SetMode method, IWMColorConvProps.SetMode, IWMColorConvProps::SetMode, SetMode, SetMode method [Media Foundation], SetMode method [Media Foundation],IWMColorConvProps interface, codecapi.iwmcolorconvpropssetmode, mf.iwmcolorconvpropssetmode, wmcodecdsp/IWMColorConvProps::SetMode
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMColorConvProps::SetMode
 - wmcodecdsp/IWMColorConvProps::SetMode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmcodecdsp.h
api_name:
 - IWMColorConvProps.SetMode
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

This method is equivalent to setting the <a href="/windows/desktop/medfound/mfpkey-colorconv-mode">MFPKEY_COLORCONV_MODE</a> property.

## -see-also

<a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcolorconvprops">IWMColorConvProps Interface</a>