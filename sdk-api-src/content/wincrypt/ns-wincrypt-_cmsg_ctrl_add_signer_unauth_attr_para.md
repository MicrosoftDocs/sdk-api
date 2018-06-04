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

# _CMSG_CTRL_ADD_SIGNER_UNAUTH_ATTR_PARA structure


## -description


The <b>CMSG_CTRL_ADD_SIGNER_UNAUTH_ATTR_PARA</b> structure is used to add an unauthenticated attribute to a signer of a signed message. This structure is passed to 
<a href="https://msdn.microsoft.com/a990d44d-2993-429f-b817-2a834105ecef">CryptMsgControl</a> if the <i>dwCtrlType</i> parameter is set to <b>CMSG_CTRL_ADD_SIGNER_UNAUTH_ATTR</b>.
			


## -struct-fields




### -field cbSize

Size of this structure in bytes.


### -field dwSignerIndex

Index of the signer in the <b>rgSigners</b> array of pointers of 
<a href="https://msdn.microsoft.com/f599226d-ddd7-455f-b650-74b91674d8f9">CMSG_SIGNER_ENCODE_INFO</a> structures in a signed message's 
<a href="https://msdn.microsoft.com/93138744-8316-461b-908a-1eab47e83f63">CMSG_SIGNED_ENCODE_INFO</a> structure. The unauthenticated attribute is to be added to this signer's information.


### -field blob

 




#### - BLOB

A <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_DATA_BLOB</a> structure that contains the encoded unauthenticated attribute as its <b>pbData</b> member.


## -see-also




<a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_INTEGER_BLOB</a>



<a href="https://msdn.microsoft.com/a990d44d-2993-429f-b817-2a834105ecef">CryptMsgControl</a>
 

 

