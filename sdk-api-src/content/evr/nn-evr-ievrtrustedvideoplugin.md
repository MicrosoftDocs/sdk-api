---
UID: NN:evr.IEVRTrustedVideoPlugin
title: IEVRTrustedVideoPlugin
author: windows-sdk-content
description: Enables a plug-in component for the enhanced video renderer (EVR) to work with protected media.
old-location: mf\ievrtrustedvideoplugin.htm
old-project: medfound
ms.assetid: 1dcaa01c-2596-4a22-9e2a-7f0e26d58ffe
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: 1dcaa01c-2596-4a22-9e2a-7f0e26d58ffe, IEVRTrustedVideoPlugin, IEVRTrustedVideoPlugin interface [Media Foundation], IEVRTrustedVideoPlugin interface [Media Foundation],described, evr/IEVRTrustedVideoPlugin, mf.ievrtrustedvideoplugin
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: MFVideoMixPrefs
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IEVRTrustedVideoPlugin
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IEVRTrustedVideoPlugin interface


## -description


Enables a plug-in component for the enhanced video renderer (EVR) to work with protected media.

To work in the protected media path (PMP), a custom EVR mixer or presenter must implement this interface. The EVR obtains a pointer to this interface by calling <b>QueryInterface</b> on the plug-in component.

This interface is required only if the plug-in is a trusted component, designed to work in the PMP. It is not required for playing clear content in an unprotected process.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEVRTrustedVideoPlugin</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEVRTrustedVideoPlugin</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEVRTrustedVideoPlugin</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/16bb31c3-51f7-4d9b-946c-f366fb6e5dee">CanConstrict</a>
</td>
<td align="left" width="63%">
Queries whether the plug-in can limit the effective video resolution.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dd9811f7-7a9f-4b7e-8425-cb25efe0a71d">DisableImageExport</a>
</td>
<td align="left" width="63%">
Enables or disables the ability of the plug-in to export the video image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/43242898-4812-4faa-8e0a-6e60455c9f3b">IsInTrustedVideoMode</a>
</td>
<td align="left" width="63%">
Queries whether the plug-in has any transient vulnerabilities at this time.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f2e9b199-969f-453c-8714-fa85c89a191a">SetConstriction</a>
</td>
<td align="left" width="63%">
Limits the effective video resolution.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/1c985558-d25d-4f51-978a-58c05943dab9">Enhanced Video Renderer</a>



<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>



<a href="https://msdn.microsoft.com/e88806ae-0041-4b4a-a8df-69718a651e82">Protected Media Path</a>
 

 

