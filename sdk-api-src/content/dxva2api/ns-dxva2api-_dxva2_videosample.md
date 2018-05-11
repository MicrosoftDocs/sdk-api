---
UID: NS:dxva2api._DXVA2_VideoSample
title: "_DXVA2_VideoSample"
author: windows-driver-content
description: Specifies an input sample for the IDirectXVideoProcessor::VideoProcessBlt method.
old-location: mf\dxva2_videosample.htm
old-project: medfound
ms.assetid: 040ade10-8573-4375-829d-938efa750a12
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: 040ade10-8573-4375-829d-938efa750a12, DXVA2_SampleData_RFF, DXVA2_SampleData_RFF_TFF_Present, DXVA2_SampleData_TFF, DXVA2_VideoSample, DXVA2_VideoSample structure [Media Foundation], _DXVA2_VideoSample, dxva2api/DXVA2_VideoSample, mf.dxva2_videosample
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: dxva2api.h
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
req.typenames: DXVA2_VideoSample
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	dxva2api.h
api_name:
-	DXVA2_VideoSample
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# _DXVA2_VideoSample structure


## -description



Specifies an input sample for the <a href="https://msdn.microsoft.com/4a199ad3-621e-4594-a9f8-ad6cfd560cec">IDirectXVideoProcessor::VideoProcessBlt</a> method.




## -struct-fields




### -field Start


            Start time of the sample, in 100-nanosecond units. For video substream samples, the value is zero.
          


### -field End


            End time of the sample, in 100-nanosecond units. For video substream samples, the value is zero.
          


### -field SampleFormat


<a href="https://msdn.microsoft.com/eba2c56b-8951-4dc5-91ae-1371793ce787">DXVA2_ExtendedFormat</a> structure that describes the interlacing and extended color information for the sample.
          


### -field SrcSurface


            Pointer to the <a href="https://msdn.microsoft.com/312eee39-6a5c-46b6-b145-78d5f0f9eecd">IDirect3DSurface9</a> interface of the Direct3D surface that contains the sample.
          


### -field SrcRect


            Source rectangle. The source rectangle defines which portion of the input sample is copied to the destination surface. The source rectangle is specified using pixel coordinates on the input surface.
          


### -field DstRect


            Destination rectangle. The destination rectangle defines the portion of the destination surface where the source rectangle is copied. The destination rectangle is specified using pixel coordinates on the destination surface.
          


### -field Pal


            If the input sample is for a substream and uses a palettized YUV color format, this member contains an array of <a href="https://msdn.microsoft.com/4d296764-a00a-407d-a963-62c138976ccc">DXVA2_AYUVSample8</a> structures that define the palette entries. For non-palettized pixel formats, the array elements should all be zero.
          


### -field PlanarAlpha


            Alpha value that will be applied to this input sample when it is composited.
          


### -field SampleData


            Contains additional flags. The following flags are defined.
          

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DXVA2_SampleData_RFF"></a><a id="dxva2_sampledata_rff"></a><a id="DXVA2_SAMPLEDATA_RFF"></a><dl>
<dt><b>DXVA2_SampleData_RFF</b></dt>
</dl>
</td>
<td width="60%">

                Repeat first field (RFF) bit.
              

</td>
</tr>
<tr>
<td width="40%"><a id="DXVA2_SampleData_TFF"></a><a id="dxva2_sampledata_tff"></a><a id="DXVA2_SAMPLEDATA_TFF"></a><dl>
<dt><b>DXVA2_SampleData_TFF</b></dt>
</dl>
</td>
<td width="60%">

                Top field first (TFF) bit.
              

</td>
</tr>
<tr>
<td width="40%"><a id="DXVA2_SampleData_RFF_TFF_Present"></a><a id="dxva2_sampledata_rff_tff_present"></a><a id="DXVA2_SAMPLEDATA_RFF_TFF_PRESENT"></a><dl>
<dt><b>DXVA2_SampleData_RFF_TFF_Present</b></dt>
</dl>
</td>
<td width="60%">

                If set, the RFF and TFF flags are used.
              

</td>
</tr>
</table>
 


            These flags provide a hint to the deinterlacer when it performs inverse telecine.
          


## -see-also




<a href="https://msdn.microsoft.com/4d296764-a00a-407d-a963-62c138976ccc">DXVA2_AYUVSample8</a>



<a href="https://msdn.microsoft.com/4a199ad3-621e-4594-a9f8-ad6cfd560cec">IDirectXVideoProcessor::VideoProcessBlt</a>



<a href="https://msdn.microsoft.com/39fdd724-13ca-48ab-8a55-93529d1da3b4">Media Foundation Structures</a>
 

 

