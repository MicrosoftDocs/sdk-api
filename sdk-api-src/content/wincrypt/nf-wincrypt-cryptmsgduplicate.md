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

# CryptMsgDuplicate function


## -description


The <b>CryptMsgDuplicate</b> function duplicates a cryptographic message handle by incrementing its <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">reference count</a>.


## -parameters




### -param hCryptMsg [in]

Handle of the cryptographic message to be duplicated. Duplication is done by incrementing the <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">reference count</a> of the message. A copy of the message is not made.


## -returns



The returned handle is the same as the handle input. A copy of the message is not created. When you have finished using the duplicated message handle, decrease the reference count by calling the <a href="https://msdn.microsoft.com/2478dd60-233a-4ef3-86e9-62d2a59ab28a">CryptMsgClose</a> function.




## -remarks



<b>CryptMsgDuplicate</b> is used to increase the reference count on an <b>HCRYPTMSG</b> handle so that multiple calls to 
<a href="https://msdn.microsoft.com/2478dd60-233a-4ef3-86e9-62d2a59ab28a">CryptMsgClose</a> are required to actually release the handle.


#### Examples

For an example that uses this function, see <a href="https://msdn.microsoft.com/effe4080-63c1-4f35-a5e3-e7e60754b28f">Example C Program: Encoding and Decoding a Hashed Message</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/2478dd60-233a-4ef3-86e9-62d2a59ab28a">CryptMsgClose</a>



<a href="cryptography_functions.htm">Low-level Message Functions</a>



<a href="cryptography_functions.htm">Simplified Message Functions</a>
 

 

