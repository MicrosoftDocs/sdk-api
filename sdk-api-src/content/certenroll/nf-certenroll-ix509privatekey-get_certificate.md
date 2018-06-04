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

# IX509PrivateKey::get_Certificate


## -description


The <b>Certificate</b> property specifies or retrieves a byte array that contains the certificate associated with the private key.  The byte array is represented by a Unicode-encoded string.

This property is read/write.


## -parameters


## -remarks



If the key is not open when you specify a  certificate, the certificate will be set when the key is opened. For more information, see the <a href="https://msdn.microsoft.com/library/windows/hardware/hh451153">Open</a> method.

The <b>Certificate</b> property compares the public key associated with the <a href="https://msdn.microsoft.com/72612ea4-ed45-46ac-9dad-614a9a754d83">IX509PrivateKey</a> object to the public key included in the certificate. The two keys must match.




## -see-also




<a href="https://msdn.microsoft.com/72612ea4-ed45-46ac-9dad-614a9a754d83">IX509PrivateKey</a>
 

 

