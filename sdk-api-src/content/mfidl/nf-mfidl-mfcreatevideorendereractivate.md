---
UID: NF:mfidl.MFCreateVideoRendererActivate
title: MFCreateVideoRendererActivate function
author: windows-sdk-content
description: Creates an activation object for the enhanced video renderer (EVR) media sink.
old-location: mf\mfcreatevideorendereractivate.htm
tech.root: medfound
ms.assetid: 021887fc-36af-42d4-ae46-2edc1c700110
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: 021887fc-36af-42d4-ae46-2edc1c700110, MFCreateVideoRendererActivate, MFCreateVideoRendererActivate function [Media Foundation], mf.mfcreatevideorendereractivate, mfidl/MFCreateVideoRendererActivate
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mfidl.h
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
req.lib: Mf.lib
req.dll: Mf.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mf.dll
api_name:
 - MFCreateVideoRendererActivate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MFCreateVideoRendererActivate function


## -description



Creates an activation object for the enhanced video renderer (EVR) media sink.




## -parameters




### -param hwndVideo [in]

Handle to the window where the video will be displayed.


### -param ppActivate [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/c0936e3c-3cd1-4c1e-a336-2dee7d943963">IMFActivate</a> interface. Use this interface to create the EVR. The caller must release the interface.


## -returns



The function returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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



To create the EVR, call <a href="https://msdn.microsoft.com/120b8070-6732-450d-8334-b3910f7bb4d2">IMFActivate::ActivateObject</a> on the retrieved <a href="https://msdn.microsoft.com/c0936e3c-3cd1-4c1e-a336-2dee7d943963">IMFActivate</a> pointer. (If you are using the Media Session, the Media Session automatically calls <b>ActivateObject</b> when you queue the topology.)

To configure the EVR, set any of the following attributes on the <a href="https://msdn.microsoft.com/c0936e3c-3cd1-4c1e-a336-2dee7d943963">IMFActivate</a> object before calling <a href="https://msdn.microsoft.com/120b8070-6732-450d-8334-b3910f7bb4d2">ActivateObject</a>.

<table>
<tr>
<th>Attribute</th>
<th>Description</th>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/60484f87-7588-4b52-93aa-ef8fad66d971">MF_ACTIVATE_CUSTOM_VIDEO_MIXER_ACTIVATE</a>
</td>
<td>Activation object for a custom mixer.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/a3586e6f-a2a2-4932-8b43-a076f64c5958">MF_ACTIVATE_CUSTOM_VIDEO_MIXER_CLSID</a>
</td>
<td>CLSID for a custom mixer.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/00e65718-885f-4e1f-9b06-66c7f5786851">MF_ACTIVATE_CUSTOM_VIDEO_MIXER_FLAGS</a>
</td>
<td>Flags for creating a custom mixer.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/65d88832-0969-4d85-bee2-fd0aa68e9f3b">MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_ACTIVATE</a>
</td>
<td>Activation object for a custom presenter.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/f035ee56-7582-45d3-bafe-dd9c821b6326">MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_CLSID</a>
</td>
<td>CLSID for a custom presenter.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/40893e13-bf2e-4424-ae43-2b253fc0b622">MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_FLAGS</a>
</td>
<td>Flags for creating a custom presenter.</td>
</tr>
</table>
 

When <a href="https://msdn.microsoft.com/120b8070-6732-450d-8334-b3910f7bb4d2">IMFActivate::ActivateObject</a> is called, the activation objects sets the video window on the EVR by calling <a href="https://msdn.microsoft.com/5dc789b7-e206-4f1d-a0b2-12cb98ce4184">IMFVideoDisplayControl::SetVideoPosition</a>. Passing <b>NULL</b> for the <i>hwndVideo</i> parameter is not an error, but no video will render unless the EVR has a valid video window.




## -see-also




<a href="https://msdn.microsoft.com/767d5f1c-2b8d-43b6-916b-035129e93204">Activation Objects</a>



<a href="https://msdn.microsoft.com/1c985558-d25d-4f51-978a-58c05943dab9">Enhanced Video Renderer</a>



<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

