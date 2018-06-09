---
UID: NN:mbnapi.IMbnConnectionProfile
title: IMbnConnectionProfile
author: windows-sdk-content
description: This interface accesses connection parameters and preferences stored in Mobile Broadband profiles.
old-location: mbn\imbnconnectionprofile.htm
old-project: mbn
ms.assetid: f7730efe-e367-4642-8482-2a23052bab0c
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: IMbnConnectionProfile, IMbnConnectionProfile interface [Microsoft Broadband Networks], IMbnConnectionProfile interface [Microsoft Broadband Networks],described, mbn.imbnconnectionprofile, mbnapi/IMbnConnectionProfile
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mbnapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: MBN_VOICE_CLASS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mbnapi.h
api_name:
 - IMbnConnectionProfile
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMbnConnectionProfile interface


## -description


This interface accesses connection parameters and preferences stored in Mobile Broadband profiles.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMbnConnectionProfile</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMbnConnectionProfile</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMbnConnectionProfile</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4de7da76-c873-4a57-a021-17436d1a64a4">Delete</a>
</td>
<td align="left" width="63%">
Deletes the profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4a94dd33-1dad-4d0a-98e8-1ccce83f345e">GetProfileXmlData</a>
</td>
<td align="left" width="63%">
Gets the XML data of the current profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3243ffec-1897-4f26-853d-81a7198a892d">UpdateProfile</a>
</td>
<td align="left" width="63%">
Updates the contents of the profile.

</td>
</tr>
</table> 


## -remarks



<b>IMbnConnectionProfile</b> objects are provided by calls to the <a href="https://msdn.microsoft.com/24658f8b-a34f-4821-9fac-bd5c8810725f">GetConnectionProfile</a> and <a href="https://msdn.microsoft.com/96752181-1135-4dcf-9c07-056dfbf2ca5f">GetConnectionProfiles</a> methods of the <a href="https://msdn.microsoft.com/a55e4183-f914-4064-a391-3bd31ca59160">IMbnConnectionProfileManager</a> interface.



