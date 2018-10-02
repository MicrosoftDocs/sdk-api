---
UID: NF:mfidl.IMFNetCredentialManager.EndGetCredentials
title: IMFNetCredentialManager::EndGetCredentials
author: windows-sdk-content
description: Completes an asynchronous request to retrieve the user's credentials.
old-location: mf\imfnetcredentialmanager_endgetcredentials.htm
tech.root: MedFound
ms.assetid: 99914ded-1b9a-4373-9974-e1d1b1abd4e2
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: 99914ded-1b9a-4373-9974-e1d1b1abd4e2, EndGetCredentials, EndGetCredentials method [Media Foundation], EndGetCredentials method [Media Foundation],IMFNetCredentialManager interface, IMFNetCredentialManager interface [Media Foundation],EndGetCredentials method, IMFNetCredentialManager.EndGetCredentials, IMFNetCredentialManager::EndGetCredentials, mf.imfnetcredentialmanager_endgetcredentials, mfidl/IMFNetCredentialManager::EndGetCredentials
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IMFNetCredentialManager.EndGetCredentials
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFNetCredentialManager::EndGetCredentials


## -description



Completes an asynchronous request to retrieve the user's credentials.




## -parameters




### -param pResult [in]

Pointer to an <a href="https://msdn.microsoft.com/8c95b1de-8974-445c-8070-41552ea83e53">IMFAsyncResult</a> interface that contains the asynchronous result.


### -param ppCred [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/d202e7bc-9ce0-4861-8552-5a4d599b1661">IMFNetCredential</a> interface, which is used to retrieve the credentials. The caller must release the interface.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/002d8608-4ef9-40fd-8dcc-fe6ade34478e">IMFNetCredentialManager</a>
 

 

