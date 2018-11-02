---
UID: NF:evr.IMFVideoMixerControl.SetStreamOutputRect
title: IMFVideoMixerControl::SetStreamOutputRect
author: windows-sdk-content
description: Sets the position of a video stream within the composition rectangle.
old-location: mf\imfvideomixercontrol_setstreamoutputrect.htm
tech.root: medfound
ms.assetid: 7075b8cf-2106-4b13-abc7-8aedae18bb62
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: 7075b8cf-2106-4b13-abc7-8aedae18bb62, IMFVideoMixerControl interface [Media Foundation],SetStreamOutputRect method, IMFVideoMixerControl.SetStreamOutputRect, IMFVideoMixerControl::SetStreamOutputRect, SetStreamOutputRect, SetStreamOutputRect method [Media Foundation], SetStreamOutputRect method [Media Foundation],IMFVideoMixerControl interface, evr/IMFVideoMixerControl::SetStreamOutputRect, mf.imfvideomixercontrol_setstreamoutputrect
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - strmiids.lib
 - strmiids.dll
api_name:
 - IMFVideoMixerControl.SetStreamOutputRect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFVideoMixerControl::SetStreamOutputRect


## -description


Sets the position of a video stream within the composition rectangle.
        


## -parameters




### -param dwStreamID [in]

Identifier of the stream. For the EVR media sink, the stream identifier is defined when the <a href="https://msdn.microsoft.com/1b05ef87-5559-4310-942c-54ab113eb42d">IMFMediaSink::AddStreamSink</a> method is called. For the DirectShow EVR filter, the stream identifier corresponds to the pin index. The reference stream is always stream 0.


### -param pnrcOutput [in]

Pointer to an <a href="https://msdn.microsoft.com/c1dd42ca-64a0-4f30-82e1-eda3f4721526">MFVideoNormalizedRect</a> structure that defines the bounding rectangle for the video stream.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The coordinates of the bounding rectangle given in <i>pnrcOutput</i> are not valid.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDSTREAMNUMBER</b></dt>
</dl>
</td>
<td width="60%">
Invalid stream identifier.
              

</td>
</tr>
</table>
 




## -remarks



The mixer draws each video stream inside a bounding rectangle that is specified relative to the final video image. This bounding rectangle is given in <i>normalized</i> coordinates. For more information, see <a href="https://msdn.microsoft.com/c1dd42ca-64a0-4f30-82e1-eda3f4721526">MFVideoNormalizedRect</a> structure.
      

The coordinates of the bounding rectangle must fall within the range [0.0, 1.0]. Also, the X and Y coordinates of the upper-left corner cannot exceed the X and Y coordinates of the lower-right corner. In other words, the bounding rectangle must fit entirely within the composition rectangle and cannot be flipped vertically or horizontally.
      

The following diagram shows how the EVR mixes substreams.

<img alt="Diagram showing an image, then that image inside a larger output rectangle, then a portion of the image in a source rectangle" border="" src="./images/d87d365f-a004-4896-ad03-48cd28449403.gif"/>
The output rectangle for the stream is specified by calling <b>SetStreamOutputRect</b>. The source rectangle is specified by calling <a href="https://msdn.microsoft.com/5dc789b7-e206-4f1d-a0b2-12cb98ce4184">IMFVideoDisplayControl::SetVideoPosition</a>. The mixer applies the output rectangle first, when it mixes the streams into a single bounding rectangle. This bounding rectangle is called <i>composition space</i>. Then the presenter applies the source rectangle to the composited image.




## -see-also




<a href="https://msdn.microsoft.com/1c985558-d25d-4f51-978a-58c05943dab9">Enhanced Video Renderer</a>



<a href="https://msdn.microsoft.com/8b5f54e3-c6da-4201-857a-9c718ad911db">IMFVideoMixerControl</a>
 

 

