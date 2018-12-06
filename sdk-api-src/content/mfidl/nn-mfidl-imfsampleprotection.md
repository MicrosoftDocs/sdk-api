---
UID: NN:mfidl.IMFSampleProtection
title: IMFSampleProtection
author: windows-sdk-content
description: Provides encryption for media data inside the protected media path (PMP).
old-location: mf\imfsampleprotection.htm
tech.root: medfound
ms.assetid: bebe24cd-657b-4c6c-9fe9-5d6dd58827a3
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IMFSampleProtection, IMFSampleProtection interface [Media Foundation], IMFSampleProtection interface [Media Foundation],described, bebe24cd-657b-4c6c-9fe9-5d6dd58827a3, mf.imfsampleprotection, mfidl/IMFSampleProtection
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
 - IMFSampleProtection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFSampleProtection interface


## -description


Provides encryption for media data inside the protected media path (PMP).
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFSampleProtection</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFSampleProtection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFSampleProtection</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/26f92775-f8a0-4b85-8cfc-353349325706">GetInputProtectionVersion</a>
</td>
<td align="left" width="63%">
Retrieves the version of sample protection that the component implements on input.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/607e6123-0cfa-4946-b390-1c44e502b2db">GetOutputProtectionVersion</a>
</td>
<td align="left" width="63%">
Retrieves the version of sample protection that the component implements on output.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b93ecc4e-40f6-4ae1-9a1a-9767e6c8c4af">GetProtectionCertificate</a>
</td>
<td align="left" width="63%">
Retrieves the sample protection certificate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2bd43f33-8528-4e78-97d5-2af39a2ac06b">InitInputProtection</a>
</td>
<td align="left" width="63%">
Initializes sample protection on the downstream component.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/03bee13d-1c51-4b26-98bb-bac15264aa54">InitOutputProtection</a>
</td>
<td align="left" width="63%">
Retrieves initialization information for sample protection from the upstream component.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

