---
UID: NN:wmsdkidl.IWMCredentialCallback
title: IWMCredentialCallback
author: windows-sdk-content
description: The IWMCredentialCallback interface is a callback interface used by the reader object to acquire user credentials.
old-location: wmformat\iwmcredentialcallback.htm
old-project: wmformat
ms.assetid: 846d4e21-5255-491a-a8aa-5bb19b62a050
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: IWMCredentialCallback, IWMCredentialCallback interface [windows Media Format], IWMCredentialCallback interface [windows Media Format],described, IWMCredentialCallbackInterface, wmformat.iwmcredentialcallback, wmsdkidl/IWMCredentialCallback
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: wmsdkidl.h
req.include-header: 
req.target-type: Windows
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
tech.root: 
req.typenames: WM_AETYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wmsdkidl.h
api_name:
-	IWMCredentialCallback
product: Windows
targetos: Windows
req.lib: Wmvcore.lib
req.dll: Wmvcore.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMCredentialCallback interface


## -description



The <b>IWMCredentialCallback</b> interface is a callback interface used by the reader object to acquire user credentials. When the reader object receives an authentication challenge from the server, it calls the application's <b>AcquireCredentials</b> method to get the credentials of the user, in order to access the remote site. This interface is implemented by the application.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMCredentialCallback</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWMCredentialCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMCredentialCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5dce8281-b5d3-42cd-93f6-d76af0050a89">AcquireCredentials</a>
</td>
<td align="left" width="63%">
Acquires the credentials of the user, to verify that the user has permission to access a remote site.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/mt427474">Authentication</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>



<a href="https://msdn.microsoft.com/b5edbf8b-820f-4e09-a482-8efc2283360e">Reader Object</a>
 

 

