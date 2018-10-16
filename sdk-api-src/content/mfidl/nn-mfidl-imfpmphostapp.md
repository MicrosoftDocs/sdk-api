---
UID: NN:mfidl.IMFPMPHostApp
title: IMFPMPHostApp
author: windows-sdk-content
description: Allows a media source to create a Windows Runtime object in the Protected Media Path (PMP) process.
old-location: mf\imfpmphostapp.htm
tech.root: medfound
ms.assetid: ca24930d-bd1e-4c12-8246-1e505a98944a
ms.author: windowssdkdev
ms.date: 10/15/2018
ms.keywords: IMFPMPHostApp, IMFPMPHostApp interface [Media Foundation], IMFPMPHostApp interface [Media Foundation],described, mf.imfpmphostapp, mfidl/IMFPMPHostApp
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - mfidl.h
api_name:
 - IMFPMPHostApp
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFPMPHostApp interface


## -description


Allows a media source to create a <a href="https://msdn.microsoft.com/0F8E8DC8-AAFA-4F4F-A81A-42AF5867FC5A">Windows Runtime</a> object in the <a href="https://msdn.microsoft.com/e88806ae-0041-4b4a-a8df-69718a651e82">Protected Media Path</a> (PMP) process.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFPMPHostApp</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFPMPHostApp</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFPMPHostApp</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e0e14171-fcc9-418a-a93d-3cdbae254a3f">ActivateClassById</a>
</td>
<td align="left" width="63%">
Runtime class of the Windows Runtime object to create.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ee3da924-a90a-4736-812e-f392631177c2">LockProcess</a>
</td>
<td align="left" width="63%">
Blocks the PMP process from ending.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4cb26f53-7d2a-417b-9bb8-0268920cf2a7">UnlockProcess</a>
</td>
<td align="left" width="63%">
Decrements the lock count on the PMP process.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>



<a href="https://msdn.microsoft.com/CF3A427D-31D2-45FF-BE87-F192B758204E">PMP Media Session</a>



<a href="https://msdn.microsoft.com/e88806ae-0041-4b4a-a8df-69718a651e82">Protected Media Path</a>
 

 

