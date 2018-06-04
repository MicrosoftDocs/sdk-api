---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IMFInputTrustAuthority interface


## -description


Enables other components in the protected media path (PMP) to use the input protection system provided by an input trust authorities (ITA). An ITA is a component that implements an input protection system for media content. ITAs expose the <b>IMFInputTrustAuthority</b> interface.

An ITA translates policy from the content's native format into a common format that is used by other PMP components. It also provides a decrypter, if one is needed to decrypt the stream.

The topology contains one ITA instance for every protected stream in the media source. The ITA is obtained from the media source by calling <a href="https://msdn.microsoft.com/b4ebf02e-554a-4e7e-93d3-6f37d8b689bf">IMFTrustedInput::GetInputTrustAuthority</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFInputTrustAuthority</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFInputTrustAuthority</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFInputTrustAuthority</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/94e447af-9311-4a2c-9ec5-be371684f79d">BindAccess</a>
</td>
<td align="left" width="63%">
Notifies the ITA that a requested action is about to be performed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3bc4e2e6-41a8-4751-a7fe-5e1f8c136983">GetDecrypter</a>
</td>
<td align="left" width="63%">
Retrieves a decrypter transform.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4d840b56-47e0-4c2f-b2e7-a17586dad8d1">GetPolicy</a>
</td>
<td align="left" width="63%">
Retrieves the policy that defines which output protection systems are allowed for this stream, and the configuration data for each protection system.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8f2f7f65-7000-4404-8678-ba36c5c97c80">RequestAccess</a>
</td>
<td align="left" width="63%">
Requests permission to perform a specified action on the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926942">Reset</a>
</td>
<td align="left" width="63%">
Resets the ITA to its initial state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4ca635fc-15eb-4a9e-8f59-7fa2e3f3e176">UpdateAccess</a>
</td>
<td align="left" width="63%">
Notifies the ITA when the number of output trust authorities (OTAs) that will perform a specified action has changed.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

