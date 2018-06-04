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

# IWMCredentialCallback::AcquireCredentials


## -description



The <b>AcquireCredentials</b> method acquires the credentials of the user, to verify that the user has permission to access a remote site.




## -parameters




### -param pwszRealm [in]

Pointer to a wide-character null-terminated string that contains the name of the realm.


### -param pwszSite [in]

Pointer to a wide-character null-terminated string containing the name of the site. The site is the name of the remote server.


### -param pwszUser [in, out]

Pointer to a buffer for the user name. The application should copy the user name into this buffer. When this method is first called, the buffer is empty. If the method is called again — for example, if the user typed his or her credentials incorrectly — the buffer may contain the name from the previous invocation.


### -param cchUser [in]

Specifies the size of the <i>pwszUser</i> buffer, in number of wide characters.


### -param pwszPassword [in, out]

Pointer to a buffer for the password. The application should copy the user's password into this buffer.


### -param cchPassword [in]

Specifies the size of the <i>pwszPassword</i> buffer, in number of wide characters.


### -param hrStatus [in]

Specifies an <b>HRESULT</b> return code.


### -param pdwFlags [in, out]

Pointer to a <b>DWORD</b> containing a bitwise <b>OR</b> of zero or more flags from the <a href="https://msdn.microsoft.com/a03e54e8-682d-4fbd-bd5c-38f58620d0d4">WMT_CREDENTIAL_FLAGS</a> enumeration type. On input, the caller sets whichever flags are relevant. On output, the application should clear the flags that were set by the caller, and set any additional flags, as appropriate. For details, see <b>WMT_CREDENTIAL_FLAGS</b>.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -remarks



This method is used when a request for a remote URL requires authentication.

The reader object calls the <b>AcquireCredentials</b> method on the application to retrieve the user name and password of the user.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/mt427474">Authentication</a>



<a href="https://msdn.microsoft.com/846d4e21-5255-491a-a8aa-5bb19b62a050">IWMCredentialCallback Interface</a>
 

 

