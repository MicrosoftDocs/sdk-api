---
UID: NN:mfidl.IMFPMPClient
title: IMFPMPClient
author: windows-sdk-content
description: Enables a media source to receive a pointer to the IMFPMPHost interface.
old-location: mf\imfpmpclient.htm
tech.root: medfound
ms.assetid: adfba5dd-eae6-48f3-a155-65bd491c952c
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: IMFPMPClient, IMFPMPClient interface [Media Foundation], IMFPMPClient interface [Media Foundation],described, adfba5dd-eae6-48f3-a155-65bd491c952c, mf.imfpmpclient, mfidl/IMFPMPClient
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFPMPClient
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFPMPClient interface


## -description


Enables a media source to receive a pointer to the <a href="https://msdn.microsoft.com/fab1fb42-07c5-4a74-b6f5-0950b2c3ba46">IMFPMPHost</a> interface.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFPMPClient</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFPMPClient</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFPMPClient</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d6e48f36-7896-4e6d-ba10-d8c0288ccffc">SetPMPHost</a>
</td>
<td align="left" width="63%">
Provides a pointer to the <a href="https://msdn.microsoft.com/fab1fb42-07c5-4a74-b6f5-0950b2c3ba46">IMFPMPHost</a> interface.
        

</td>
</tr>
</table> 


## -remarks



If a media source exposes this interface, the Protected Media Path (PMP) Media Session calls <a href="https://msdn.microsoft.com/d6e48f36-7896-4e6d-ba10-d8c0288ccffc">SetPMPHost</a> with a pointer to the <a href="https://msdn.microsoft.com/fab1fb42-07c5-4a74-b6f5-0950b2c3ba46">IMFPMPHost</a> interface. The media source can use the <b>IMFPMPHost</b> interface to create objects in the PMP process.




## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>



<a href="https://msdn.microsoft.com/CF3A427D-31D2-45FF-BE87-F192B758204E">PMP Media Session</a>



<a href="https://msdn.microsoft.com/e88806ae-0041-4b4a-a8df-69718a651e82">Protected Media Path</a>
 

 

