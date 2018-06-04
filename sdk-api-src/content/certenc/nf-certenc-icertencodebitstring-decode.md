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

# ICertEncodeBitString::Decode


## -description


The <b>Decode</b> method decodes an <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Abstract Syntax Notation One</a> (ASN.1)-encoded bit string and stores the resulting bit string in this object. You can then call the 
<a href="https://msdn.microsoft.com/9fbaaf03-02b8-4c6f-8cc2-3fd897fdc81d">ICertEncodeBitString::GetBitCount</a> and 
<a href="https://msdn.microsoft.com/d0c6c501-3aaa-42ab-a077-69f6d24f1eff">ICertEncodeBitString::GetBitString</a> methods to retrieve the bit string and its size.


## -parameters




### -param strBinary [in]

An ASN.1-encoded bit string.


## -returns



<h3>VB</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see 
<a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



Use this method to decode an encoded bit string.


#### Examples

For an example that calls the <b>Decode</b> method, see the <a href="https://msdn.microsoft.com/2dc74ab4-8f40-4e0d-a18e-ba9c99d5bf94">ICertEncodeBitString::Encode</a> method.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/51178b67-46da-49f8-9bd7-a500e846e0a8">ICertEncodeBitString</a>



<a href="https://msdn.microsoft.com/2dc74ab4-8f40-4e0d-a18e-ba9c99d5bf94">ICertEncodeBitString::Encode</a>
 

 

