---
UID: NN:opmapi.IOPMVideoOutput
title: IOPMVideoOutput
author: windows-sdk-content
description: Represents a video output for an Output Protection Manager (OPM) session.
old-location: mf\iopmvideooutput.htm
tech.root: MedFound
ms.assetid: 8bf43577-3535-4f62-ac81-bb7e3c329403
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IOPMVideoOutput, IOPMVideoOutput interface [Media Foundation], IOPMVideoOutput interface [Media Foundation],described, mf.iopmvideooutput, opmapi/IOPMVideoOutput
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: opmapi.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - opmapi.h
api_name:
 - IOPMVideoOutput
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOPMVideoOutput interface


## -description


Represents a video output for an <a href="https://msdn.microsoft.com/daae615b-37c4-4044-91c6-693357e0016a">Output Protection Manager</a> (OPM) session.

To get a pointer to this interface, call one of the following functions:
<ul>
<li>
<a href="https://msdn.microsoft.com/9b287058-9e06-4c40-84f4-506aefce5b8a">OPMGetVideoOutputsFromIDirect3DDevice9Object</a>
</li>
<li>
<a href="https://msdn.microsoft.com/c034ac81-43d4-482a-9dad-234d33a15046">OPMGetVideoOutputsFromHMONITOR</a>
</li>
</ul>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOPMVideoOutput</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IOPMVideoOutput</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOPMVideoOutput</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b8eb3561-7e81-4f4c-bcb1-1657f8556aea">Configure</a>
</td>
<td align="left" width="63%">
Configures a video output.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/46c0c426-9730-4a0e-ab95-03b240bd55f0">COPPCompatibleGetInformation</a>
</td>
<td align="left" width="63%">
Sends a status request to the display driver. Use this method when OPM is emulating Certified Output Protection Manager (COPP).



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7551e374-8745-405b-9879-d35a92d661ea">FinishIntialization</a>
</td>
<td align="left" width="63%">
Completes the initialization sequence for an OPM session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/47d724eb-07e9-4659-886a-4b492fbb2415">GetInformation</a>
</td>
<td align="left" width="63%">
Sends a status request to the display driver.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/eeedeb4b-753f-4efb-b8ef-732cce116b42">StartInitialization</a>
</td>
<td align="left" width="63%">
Begins the initialization sequence for an OPM session.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>



<a href="https://msdn.microsoft.com/c3eabc15-0c0f-4deb-9b7a-ec9ce6ce6bb4">OPM Interfaces</a>



<a href="https://msdn.microsoft.com/daae615b-37c4-4044-91c6-693357e0016a">Output Protection Manager</a>
 

 

