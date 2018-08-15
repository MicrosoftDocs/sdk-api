---
UID: NN:mfidl.IMFNetCredentialManager
title: IMFNetCredentialManager
author: windows-sdk-content
description: Implemented by applications to provide user credentials for a network source.
old-location: mf\imfnetcredentialmanager.htm
old-project: medfound
ms.assetid: 002d8608-4ef9-40fd-8dcc-fe6ade34478e
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: 002d8608-4ef9-40fd-8dcc-fe6ade34478e, IMFNetCredentialManager, IMFNetCredentialManager interface [Media Foundation], IMFNetCredentialManager interface [Media Foundation],described, mf.imfnetcredentialmanager, mfidl/IMFNetCredentialManager
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: mfidl.h
req.include-header: 
req.redist: 
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
 - IMFNetCredentialManager
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: Mfplat.dll
req.irql: 
req.product: GDI+ 1.1
---

# IMFNetCredentialManager interface


## -description


Implemented by applications to provide user credentials for a network source.

To use this interface, implement it in your application. Then create a property store object and set the <a href="https://msdn.microsoft.com/c0826956-9df1-40ec-8ad1-9e0dca34d847">MFNETSOURCE_CREDENTIAL_MANAGER</a> property. The value of the property is a pointer to your application's <b>IMFNetCredentialManager</b> interface. Then pass the property store to one of the source resolver's creation functions, such as <a href="https://msdn.microsoft.com/b8f751b1-6456-4d67-839d-ecfa388e8d71">IMFSourceResolver::CreateObjectFromURL</a>, in the <i>pProps</i> parameter.

Media Foundation does not provide a default implementation of this interface. Applications that support authentication must implement this interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFNetCredentialManager</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFNetCredentialManager</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFNetCredentialManager</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ff11ff99-18bf-4c4c-93fd-31c06309f105">BeginGetCredentials</a>
</td>
<td align="left" width="63%">
Begins an asynchronous request to retrieve the user's credentials.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/99914ded-1b9a-4373-9974-e1d1b1abd4e2">EndGetCredentials</a>
</td>
<td align="left" width="63%">
Completes an asynchronous request to retrieve the user's credentials.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f58e30ba-3e9b-41b5-9c13-0f9dac541033">SetGood</a>
</td>
<td align="left" width="63%">
Specifies whether the user's credentials succeeded in the authentication challenge.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>



<a href="https://msdn.microsoft.com/bffc33ec-0fb0-4bbe-9bac-583b9d4e1153">Network Source Authentication</a>
 

 

