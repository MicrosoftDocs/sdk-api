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

# DavAddConnection function


## -description


Creates a secure connection to a WebDAV server or to a remote file or directory on a WebDAV server.


## -parameters




### -param ConnectionHandle [in, out]

A pointer to a variable that receives the connection handle.


### -param RemoteName [in]

A pointer to a <b>null</b>-terminated Unicode string that contains the path to the remote file or directory. This string must begin with the "https://" prefix.


### -param UserName [in, optional]

A pointer to a <b>null</b>-terminated Unicode string that contains the user name to be used for the connection. This parameter is optional and can be <b>NULL</b>.


### -param Password [in, optional]

A pointer to a <b>null</b>-terminated Unicode string that contains the password to be used for the connection. This parameter is optional and can be <b>NULL</b>.


### -param ClientCert [in]

A pointer to a buffer that contains the client certificate to be used for the connection. The certificate must be in a serialized form.


### -param CertSize [in]

Size, in bytes, of the client certificate.


## -returns



If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is a <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>.




## -remarks



To close the connection, use the <a href="https://msdn.microsoft.com/736b8a16-30db-410e-8295-97730297d04b">DavDeleteConnection</a> function.

Use this function when you are connecting to a WebDAV server using the Secure Sockets Layer (SSL) protocol and therefore must specify a certificate. To connect to a WebDAV server without specifying a certificate, use a Windows networking function such as <a href="https://msdn.microsoft.com/faec728c-f19e-418c-9bdb-cde93e7d98fb">WNetAddConnection2</a> or <a href="https://msdn.microsoft.com/169c7bb4-cb08-424c-af79-2133684a99db">WNetAddConnection3</a>.




## -see-also




<a href="https://msdn.microsoft.com/23699439-1a6c-4907-93fa-651024856be7">CertOpenSystemStore</a>
 

 

