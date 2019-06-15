---
UID: NN:vmr9.IVMRDeinterlaceControl9
title: IVMRDeinterlaceControl9 (vmr9.h)
author: windows-sdk-content
description: The IVMRDeinterlaceControl9 interface supports hardware-accelerated deinterlacing using the Video Mixing Renderer Filter 9 (VMR-9).
old-location: dshow\ivmrdeinterlacecontrol9.htm
tech.root: DirectShow
ms.assetid: 685f3627-30bd-4c78-9eda-0b06203dd46e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IVMRDeinterlaceControl9, IVMRDeinterlaceControl9 interface [DirectShow], IVMRDeinterlaceControl9 interface [DirectShow],described, IVMRDeinterlaceControl9Interface, dshow.ivmrdeinterlacecontrol9, vmr9/IVMRDeinterlaceControl9
ms.topic: interface
req.header: vmr9.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
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
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IVMRDeinterlaceControl9
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVMRDeinterlaceControl9 interface


## -description


The <b>IVMRDeinterlaceControl9</b> interface supports hardware-accelerated deinterlacing using the <a href="https://docs.microsoft.com/windows/desktop/DirectShow/video-mixing-renderer-filter-9">Video Mixing Renderer Filter 9</a> (VMR-9). This interface enables applications or other filters to control how the VMR manages DirectX Video Acceleration (DirectX VA) hardware deinterlacing.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVMRDeinterlaceControl9</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVMRDeinterlaceControl9</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVMRDeinterlaceControl9</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getactualdeinterlacemode">GetActualDeinterlaceMode</a>
</td>
<td align="left" width="63%">
Returns the deinterlacing mode that the VMR is using for a specified stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getdeinterlacemode">GetDeinterlaceMode</a>
</td>
<td align="left" width="63%">
Retrieves the deinterlacing mode for the specified video stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getdeinterlacemodecaps">GetDeinterlaceModeCaps</a>
</td>
<td align="left" width="63%">
Retrieves the capabilities of a specific deinterlacing mode supported by the graphics device driver.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getdeinterlaceprefs">GetDeinterlacePrefs</a>
</td>
<td align="left" width="63%">
Queries how the VMR will select a deinterlacing mode if it cannot use the preferred mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getnumberofdeinterlacemodes">GetNumberOfDeinterlaceModes</a>
</td>
<td align="left" width="63%">
Retrieves the deinterlacing modes available to the VMR for the specified video format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vmr9/nf-vmr9-ivmrdeinterlacecontrol9-setdeinterlacemode">SetDeinterlaceMode</a>
</td>
<td align="left" width="63%">
Sets the deinterlacing mode for the specified video stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vmr9/nf-vmr9-ivmrdeinterlacecontrol9-setdeinterlaceprefs">SetDeinterlacePrefs</a>
</td>
<td align="left" width="63%">
Specifies how the VMR will select a deinterlacing mode if it cannot use the preferred mode.

</td>
</tr>
</table> 


## -remarks



Deinterlacing modes are identified by GUIDs. The graphics device driver returns an array of GUIDs for the modes that it supports. The array is sorted in order of quality, from best quality to lowest quality. To retrieve the list of GUIDs, call the <a href="https://docs.microsoft.com/windows/desktop/api/vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getnumberofdeinterlacemodes">GetNumberOfDeinterlaceModes</a> method. To obtain more information about a particular mode, pass this GUID to the <a href="https://docs.microsoft.com/windows/desktop/api/vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getdeinterlacemodecaps">GetDeinterlaceModeCaps</a> method. To configure the VMR to use a particular mode, call the <a href="https://docs.microsoft.com/windows/desktop/api/vmr9/nf-vmr9-ivmrdeinterlacecontrol9-setdeinterlacemode">SetDeinterlaceMode</a> method.

To determine what de-interlacing modes are available, perform these steps:

<ol>
<li>Create the VMR-9 and put it into mixing mode.
      </li>
<li>Query the VMR-9 for the <b>IVMRDeinterlaceControl9</b> interface</li>
<li>Fill in a <a href="https://docs.microsoft.com/windows/desktop/api/strmif/ns-strmif-_vmrvideodesc">VMRVideoDesc</a> structure that describes the format of the interlaced video.</li>
<li>Call <a href="https://docs.microsoft.com/windows/desktop/api/vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getnumberofdeinterlacemodes">IVMRDeinterlaceControl9::GetNumberOfDeinterlaceModes</a> to get the number of available de-interlacing modes.</li>
<li>For each mode returned, call <a href="https://docs.microsoft.com/windows/desktop/api/vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getdeinterlacemodecaps">IVMRDeinterlaceControl::GetDeinterlaceModeCaps</a> to get information about the mode.</li>
</ol>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/setting-deinterlace-preferences">Setting Deinterlace Preferences</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/video-mixing-renderer-filter-9">Video Mixing Renderer Filter 9</a>
 

 

