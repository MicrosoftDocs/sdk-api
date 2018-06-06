---
UID: NN:mfidl.IMFNetCredentialCache
title: IMFNetCredentialCache
author: windows-sdk-content
description: Gets credentials from the credential cache.
old-location: mf\imfnetcredentialcache.htm
old-project: medfound
ms.assetid: d02e26e7-e99c-4be7-8495-830eff2f1554
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: IMFNetCredentialCache, IMFNetCredentialCache interface [Media Foundation], IMFNetCredentialCache interface [Media Foundation],described, d02e26e7-e99c-4be7-8495-830eff2f1554, mf.imfnetcredentialcache, mfidl/IMFNetCredentialCache
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
tech.root: 
req.typenames: MFSensorDeviceMode
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFNetCredentialCache
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: Mfplat.dll
req.irql: 
req.product: GDI+ 1.1
---

# IMFNetCredentialCache interface


## -description


Gets credentials from the credential cache.

This interface is implemented by the credential cache object. Applications that implement the <a href="https://msdn.microsoft.com/002d8608-4ef9-40fd-8dcc-fe6ade34478e">IMFNetCredentialManager</a> interface can use this object to store the user's credentials. To create the credential cache object, call <a href="https://msdn.microsoft.com/ec27f54a-4534-4342-856b-f6f55c5a7fdb">MFCreateCredentialCache</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFNetCredentialCache</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFNetCredentialCache</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFNetCredentialCache</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7e095445-354a-4fbb-b354-bf87eb77552f">GetCredential</a>
</td>
<td align="left" width="63%">
Gets the credential object for the specified URL.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e2e9d87a-6238-49a0-9a19-fe213749d627">SetGood</a>
</td>
<td align="left" width="63%">
Specifies whether the credential object provided successfully passed the authentication challenge.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/024eea57-e7c8-495d-9959-ab37dd45873d">SetUserOptions</a>
</td>
<td align="left" width="63%">
Specifies how user credentials are persisted.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>



<a href="https://msdn.microsoft.com/bffc33ec-0fb0-4bbe-9bac-583b9d4e1153">Network Source Authentication</a>
 

 

