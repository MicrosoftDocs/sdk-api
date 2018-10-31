---
UID: NN:mfidl.IMFNetCredential
title: IMFNetCredential
author: windows-sdk-content
description: Sets and retrieves user-name and password information for authentication purposes.
old-location: mf\imfnetcredential.htm
tech.root: medfound
ms.assetid: d202e7bc-9ce0-4861-8552-5a4d599b1661
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: IMFNetCredential, IMFNetCredential interface [Media Foundation], IMFNetCredential interface [Media Foundation],described, d202e7bc-9ce0-4861-8552-5a4d599b1661, mf.imfnetcredential, mfidl/IMFNetCredential
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
 - IMFNetCredential
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFNetCredential interface


## -description


Sets and retrieves user-name and password information for authentication purposes.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFNetCredential</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFNetCredential</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFNetCredential</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ab7a4999-4a08-472c-bb7e-7068f2e2ac34">GetPassword</a>
</td>
<td align="left" width="63%">
Retrieves the decrypted password.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/11e10b9f-fd98-44f2-a829-d9ed3a5be189">GetUser</a>
</td>
<td align="left" width="63%">
Retrieves the username.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/70f3dc70-ed6b-417c-93cb-e00efcdb43ec">LoggedOnUser</a>
</td>
<td align="left" width="63%">
Queries whether logged on credentials should be used.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7de58b57-83fe-4c3a-9029-e9be556c84c9">SetPassword</a>
</td>
<td align="left" width="63%">
Sets the password.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/026a822a-4e48-4fc8-9781-5e427528a4d2">SetUser</a>
</td>
<td align="left" width="63%">
Sets the user name.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>



<a href="https://msdn.microsoft.com/bffc33ec-0fb0-4bbe-9bac-583b9d4e1153">Network Source Authentication</a>
 

 

