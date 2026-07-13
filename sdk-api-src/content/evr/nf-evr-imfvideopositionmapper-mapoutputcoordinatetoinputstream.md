---
UID: NF:evr.IMFVideoPositionMapper.MapOutputCoordinateToInputStream
title: IMFVideoPositionMapper::MapOutputCoordinateToInputStream (evr.h)
description: Maps output image coordinates to input image coordinates.
helpviewer_keywords: ["IMFVideoPositionMapper interface [Media Foundation]","MapOutputCoordinateToInputStream method","IMFVideoPositionMapper.MapOutputCoordinateToInputStream","IMFVideoPositionMapper::MapOutputCoordinateToInputStream","MapOutputCoordinateToInputStream","MapOutputCoordinateToInputStream method [Media Foundation]","MapOutputCoordinateToInputStream method [Media Foundation]","IMFVideoPositionMapper interface","d57aed5f-90cb-47e7-af80-f3573a3b8256","evr/IMFVideoPositionMapper::MapOutputCoordinateToInputStream","mf.imfvideopositionmapper_mapoutputcoordinatetoinputstream"]
old-location: mf\imfvideopositionmapper_mapoutputcoordinatetoinputstream.htm
tech.root: mfarchive
ms.assetid: d57aed5f-90cb-47e7-af80-f3573a3b8256
ms.date: 12/05/2018
ms.keywords: IMFVideoPositionMapper interface [Media Foundation],MapOutputCoordinateToInputStream method, IMFVideoPositionMapper.MapOutputCoordinateToInputStream, IMFVideoPositionMapper::MapOutputCoordinateToInputStream, MapOutputCoordinateToInputStream, MapOutputCoordinateToInputStream method [Media Foundation], MapOutputCoordinateToInputStream method [Media Foundation],IMFVideoPositionMapper interface, d57aed5f-90cb-47e7-af80-f3573a3b8256, evr/IMFVideoPositionMapper::MapOutputCoordinateToInputStream, mf.imfvideopositionmapper_mapoutputcoordinatetoinputstream
req.header: evr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFVideoPositionMapper::MapOutputCoordinateToInputStream
 - evr/IMFVideoPositionMapper::MapOutputCoordinateToInputStream
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - strmiids.lib
 - strmiids.dll
api_name:
 - IMFVideoPositionMapper.MapOutputCoordinateToInputStream
archived: true
---

# IMFVideoPositionMapper::MapOutputCoordinateToInputStream


## -description

[The component described on this page, [Enhanced Video Renderer](/windows/win32/medfound/enhanced-video-renderer), is a legacy feature. It has been superseded by the Simple Video Renderer (SVR) exposed through the [MediaPlayer](/uwp/api/windows.media.playback.mediaplayer) and [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine) components. To play video content you should send data into one of these components and allow them to instantiate the new video renderer.  These components have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** or the lower level **IMFMediaEngine** APIs to play video media in Windows instead of the EVR, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.]

Maps output image coordinates to input image coordinates. This method provides the reverse transformation for components that map coordinates on the input image to different coordinates on the output image.

## -parameters

### -param xOut [in]

X-coordinate of the output image, normalized to the range [0...1].

### -param yOut [in]

Y-coordinate of the output image, normalized to the range [0...1].

### -param dwOutputStreamIndex [in]

Output stream index for the coordinate mapping.

### -param dwInputStreamIndex [in]

Input stream index for the coordinate mapping.

### -param pxIn [out]

Receives the mapped x-coordinate of the input image, normalized to the range [0...1].

### -param pyIn [out]

Receives the mapped y-coordinate of the input image, normalized to the range [0...1].

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
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_SHUTDOWN</b></dt>
</dl>
</td>
<td width="60%">
The video renderer has been shut down.
              

</td>
</tr>
</table>

## -remarks

In the following diagram, R(dest) is the destination rectangle for the video. You can obtain this rectangle by calling <a href="/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-getvideoposition">IMFVideoDisplayControl::GetVideoPosition</a>. The rectangle R1 is a substream within the video. The point P has pixel coordinates (x,y) relative to R(dest).

<img alt="Illustration showing a rectangle labeled R dest surrounding one labeled R1, which contains a point P located at (x,y)" border="" src="./images/imfvideopositionmapper.gif"/>

The position of P relative to R(dest) in <i>normalized</i> coordinates is calculated as follows:


``` syntax
float xn = float(x + 0.5) / widthDest;
float xy = float(y + 0.5) / heightDest;

```

where <i>widthDest</i> and <i>heightDest</i> are the width and height of R(dest) in pixels.

To calculate the position of P relative to R1, call <b>MapOutputCoordinateToInputStream</b> as follows:


``` syntax
float x1 = 0, y1 = 0;
hr = pMap->MapOutputCoordinateToInputStream(xn, yn, 0, dwInputStreamIndex, &x1, &y1);
```

The values returned in <i>x1</i> and <i>y1</i> are normalized to the range [0...1]. To convert back to pixel coordinates, scale these values by the size of R1:


``` syntax
int scaledx = int(floor(x1 * widthR1));
int scaledy = int(floor(xy * heightR1));
```

Note that <i>x1</i> and <i>y1</i> might fall outside the range [0...1] if P lies outside of R1.

## -see-also

<a href="/windows/desktop/api/evr/nn-evr-imfvideopositionmapper">IMFVideoPositionMapper</a>
