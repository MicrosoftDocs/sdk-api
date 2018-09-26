---
UID: NN:strmif.IVMRDeinterlaceControl
title: IVMRDeinterlaceControl
author: windows-sdk-content
description: The IVMRDeinterlaceControl interface provides support for advanced hardware-accelerated deinterlacing using the Video Mixing Renderer Filter 7 (VMR-7).
old-location: dshow\ivmrdeinterlacecontrol.htm
tech.root: DirectShow
ms.assetid: 77abbcd4-6538-491d-b3c2-6a29a391c68a
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: IVMRDeinterlaceControl, IVMRDeinterlaceControl interface [DirectShow], IVMRDeinterlaceControl interface [DirectShow],described, IVMRDeinterlaceControlInterface, dshow.ivmrdeinterlacecontrol, strmif/IVMRDeinterlaceControl
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVMRDeinterlaceControl interface


## -description


The <b>IVMRDeinterlaceControl</b> interface provides support for advanced hardware-accelerated deinterlacing using the <a href="https://msdn.microsoft.com/c83e6c50-76f2-4aeb-944b-5b244c6bf776">Video Mixing Renderer Filter 7</a> (VMR-7). This interface enables applications or other filters to control how the VMR manages DirectX Video Acceleration (DirectX VA) hardware deinterlacing.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVMRDeinterlaceControl</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVMRDeinterlaceControl</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/b8b5c619-68fe-40a5-8621-ef6e9ad612d8">GetActualDeinterlaceMode</a>
</td>
<td align="left" width="63%">
Returns the deinterlacing mode that the VMR is using for a specified stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/558b4902-596a-45f9-ad95-f8e868ba4a30">GetDeinterlaceMode</a>
</td>
<td align="left" width="63%">
Retrieves the deinterlacing mode for the specified video stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e672f3d4-1009-4c4c-bb1a-08f78c128423">GetDeinterlaceModeCaps</a>
</td>
<td align="left" width="63%">
Retrieves the capabilities of a specific deinterlacing mode supported by the graphics device driver.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bb9de83c-087e-4d6e-861a-7db388d59a7c">GetDeinterlacePrefs</a>
</td>
<td align="left" width="63%">
Queries how the VMR will select a deinterlacing mode if it cannot use the preferred mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0e6abb00-95fb-453d-9427-178058b217b8">GetNumberOfDeinterlaceModes</a>
</td>
<td align="left" width="63%">
Retrieves the deinterlacing modes available to the VMR for the specified video format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1a716e10-5382-4b2b-9a4b-b3998a584956">SetDeinterlaceMode</a>
</td>
<td align="left" width="63%">
Sets the deinterlacing mode for the specified video stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5a78b8cc-ecf8-4e0a-87f0-56b7aac6abdd">SetDeinterlacePrefs</a>
</td>
<td align="left" width="63%">
Specifies how the VMR will select a deinterlacing mode if it cannot use the preferred mode.

</td>
</tr>
</table> 


## -remarks



This interface is applicable only when the VMR is in mixer mode. All methods in this interface return VFW_E_VMR_NOT_IN_MIXER_MODE if the VMR is not in mixer mode.

Deinterlacing modes are identified by GUIDs. The graphics device driver returns an array of GUIDs for the modes that it supports. The array is sorted in order of quality, from best quality to lowest quality. To retrieve the list of GUIDs, call the <a href="https://msdn.microsoft.com/0e6abb00-95fb-453d-9427-178058b217b8">GetNumberOfDeinterlaceModes</a> method. To obtain more information about a particular mode, pass this GUID to the <a href="https://msdn.microsoft.com/e672f3d4-1009-4c4c-bb1a-08f78c128423">GetDeinterlaceModeCaps</a> method. To configure the VMR to use a particular mode, call the <a href="https://msdn.microsoft.com/1a716e10-5382-4b2b-9a4b-b3998a584956">SetDeinterlaceMode</a> method.




## -see-also




<a href="https://msdn.microsoft.com/31d59f17-552b-46d1-89e4-751216f54280">Setting Deinterlace Preferences</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

