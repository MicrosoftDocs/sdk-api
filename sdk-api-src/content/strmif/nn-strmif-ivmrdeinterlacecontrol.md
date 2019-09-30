---
UID: NN:strmif.IVMRDeinterlaceControl
title: IVMRDeinterlaceControl (strmif.h)
author: windows-sdk-content
description: The IVMRDeinterlaceControl interface provides support for advanced hardware-accelerated deinterlacing using the Video Mixing Renderer Filter 7 (VMR-7).
old-location: dshow\ivmrdeinterlacecontrol.htm
tech.root: DirectShow
ms.assetid: 77abbcd4-6538-491d-b3c2-6a29a391c68a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IVMRDeinterlaceControl, IVMRDeinterlaceControl interface [DirectShow], IVMRDeinterlaceControl interface [DirectShow],described, IVMRDeinterlaceControlInterface, dshow.ivmrdeinterlacecontrol, strmif/IVMRDeinterlaceControl
ms.topic: interface
f1_keywords: 
 - "strmif/IVMRDeinterlaceControl"
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
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
 - IVMRDeinterlaceControl
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVMRDeinterlaceControl interface


## -description


The <b>IVMRDeinterlaceControl</b> interface provides support for advanced hardware-accelerated deinterlacing using the <a href="https://docs.microsoft.com/windows/desktop/DirectShow/video-mixing-renderer-filter-7">Video Mixing Renderer Filter 7</a> (VMR-7). This interface enables applications or other filters to control how the VMR manages DirectX Video Acceleration (DirectX VA) hardware deinterlacing.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVMRDeinterlaceControl</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVMRDeinterlaceControl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVMRDeinterlaceControl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ivmrdeinterlacecontrol-getactualdeinterlacemode">GetActualDeinterlaceMode</a>
</td>
<td align="left" width="63%">
Returns the deinterlacing mode that the VMR is using for a specified stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ivmrdeinterlacecontrol-getdeinterlacemode">GetDeinterlaceMode</a>
</td>
<td align="left" width="63%">
Retrieves the deinterlacing mode for the specified video stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ivmrdeinterlacecontrol-getdeinterlacemodecaps">GetDeinterlaceModeCaps</a>
</td>
<td align="left" width="63%">
Retrieves the capabilities of a specific deinterlacing mode supported by the graphics device driver.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ivmrdeinterlacecontrol-getdeinterlaceprefs">GetDeinterlacePrefs</a>
</td>
<td align="left" width="63%">
Queries how the VMR will select a deinterlacing mode if it cannot use the preferred mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ivmrdeinterlacecontrol-getnumberofdeinterlacemodes">GetNumberOfDeinterlaceModes</a>
</td>
<td align="left" width="63%">
Retrieves the deinterlacing modes available to the VMR for the specified video format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ivmrdeinterlacecontrol-setdeinterlacemode">SetDeinterlaceMode</a>
</td>
<td align="left" width="63%">
Sets the deinterlacing mode for the specified video stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ivmrdeinterlacecontrol-setdeinterlaceprefs">SetDeinterlacePrefs</a>
</td>
<td align="left" width="63%">
Specifies how the VMR will select a deinterlacing mode if it cannot use the preferred mode.

</td>
</tr>
</table> 


## -remarks



This interface is applicable only when the VMR is in mixer mode. All methods in this interface return VFW_E_VMR_NOT_IN_MIXER_MODE if the VMR is not in mixer mode.

Deinterlacing modes are identified by GUIDs. The graphics device driver returns an array of GUIDs for the modes that it supports. The array is sorted in order of quality, from best quality to lowest quality. To retrieve the list of GUIDs, call the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ivmrdeinterlacecontrol-getnumberofdeinterlacemodes">GetNumberOfDeinterlaceModes</a> method. To obtain more information about a particular mode, pass this GUID to the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ivmrdeinterlacecontrol-getdeinterlacemodecaps">GetDeinterlaceModeCaps</a> method. To configure the VMR to use a particular mode, call the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ivmrdeinterlacecontrol-setdeinterlacemode">SetDeinterlaceMode</a> method.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/setting-deinterlace-preferences">Setting Deinterlace Preferences</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>
 

 

