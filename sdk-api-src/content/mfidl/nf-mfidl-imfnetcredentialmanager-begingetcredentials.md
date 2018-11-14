---
UID: NF:mfidl.IMFNetCredentialManager.BeginGetCredentials
title: IMFNetCredentialManager::BeginGetCredentials
author: windows-sdk-content
description: Begins an asynchronous request to retrieve the user's credentials.
old-location: mf\imfnetcredentialmanager_begingetcredentials.htm
tech.root: medfound
ms.assetid: ff11ff99-18bf-4c4c-93fd-31c06309f105
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: BeginGetCredentials, BeginGetCredentials method [Media Foundation], BeginGetCredentials method [Media Foundation],IMFNetCredentialManager interface, IMFNetCredentialManager interface [Media Foundation],BeginGetCredentials method, IMFNetCredentialManager.BeginGetCredentials, IMFNetCredentialManager::BeginGetCredentials, ff11ff99-18bf-4c4c-93fd-31c06309f105, mf.imfnetcredentialmanager_begingetcredentials, mfidl/IMFNetCredentialManager::BeginGetCredentials
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
 - IMFNetCredentialManager.BeginGetCredentials
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- mfidl.h
: 
- IMFNetCredentialManager.BeginGetCredentials
: 
---

# IMFNetCredentialManager::BeginGetCredentials


## -description



Begins an asynchronous request to retrieve the user's credentials.




## -parameters




### -param pParam [in]

Pointer to an <a href="https://msdn.microsoft.com/951d74df-11f8-4623-a81b-63e632f80d0e">MFNetCredentialManagerGetParam</a> structure.


### -param pCallback [in]

Pointer to the <a href="https://msdn.microsoft.com/7edff985-da59-4cc0-96de-1a92e03a7d41">IMFAsyncCallback</a> interface of a callback object. The caller must implement this interface.


### -param pState [in]

Pointer to the <b>IUnknown</b> interface of a state object, defined by the caller. This parameter can be <b>NULL</b>. The object is returned to the caller when the callback is invoked.


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
 

 

