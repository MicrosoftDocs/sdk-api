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

# ITLegacyCallMediaControl interface


## -description


The 
<b>ITLegacyCallMediaControl</b> interface supports legacy applications that must communicate directly with a device. This interface is exposed on the 
<a href="https://msdn.microsoft.com/67c063ba-8b12-40d6-9011-923bdee8b214">Call Object</a> and can be created by calling <b>QueryInterface</b> on 
<a href="https://msdn.microsoft.com/a0b4c496-5ee8-4810-8170-8ea505c99f18">ITBasicCallControl</a>.

The 
<a href="https://msdn.microsoft.com/47fa5669-1c74-4c18-8370-3efe35b3573e">ITLegacyCallMediaControl2</a> interface is an extension of the 
<b>ITLegacyCallMediaControl</b> interface. 
<b>ITLegacyCallMediaControl2</b> provides additional methods, primarily for tone detection and generation.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITLegacyCallMediaControl</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>ITLegacyCallMediaControl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITLegacyCallMediaControl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/09adb3fb-cf77-4c8b-beab-85d173cbb242">DetectDigits</a>
</td>
<td align="left" width="63%">
Sets 
<a href="https://msdn.microsoft.com/library/windows/hardware/dn923108">mode</a> for digit detection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d4dcdce0-4df5-43bb-a5ea-ea72782d5f04">GenerateDigits</a>
</td>
<td align="left" width="63%">
Sends digits to call destination.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff546827">GetID</a>
</td>
<td align="left" width="63%">
Gets identifier for device associated with the current call. This method is intended for Visual Basic and scripting applications.

This method is intended for C/C++ applications.  Visual Basic and scripting applications should use the 
<a href="https://msdn.microsoft.com/6c28889f-3768-4136-ac73-80c6c5ffeac3">ITLegacyCallMediaControl2::GetIDAsVariant</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/82efd729-fbbf-449f-a347-24bceada140c">MonitorMedia</a>
</td>
<td align="left" width="63%">
Sets monitoring for a given media type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/627fe465-40f6-481e-9fd6-3fc3e2931e18">SetMediaType</a>
</td>
<td align="left" width="63%">
Sets 
<a href="https://msdn.microsoft.com/3e418c9a-a008-4b94-b5d2-7c2eccb3bf87">media type</a> for call.

</td>
</tr>
</table> 


## -see-also




<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>



<a href="https://msdn.microsoft.com/47fa5669-1c74-4c18-8370-3efe35b3573e">ITLegacyCallMediaControl2</a>
 

 

