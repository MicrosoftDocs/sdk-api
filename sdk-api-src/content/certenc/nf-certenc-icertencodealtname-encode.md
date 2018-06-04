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

# ICertEncodeAltName::Encode


## -description


The <b>Encode</b> method returns an ASN.1-encoded string of the alternate name array stored in this object. The names in the object are not encoded.

Use the <a href="https://msdn.microsoft.com/0507d3a5-b8c3-4f2e-996f-e1e32957f475">Decode</a> method to decode the encoded string into an <b>CertEncodeAltName</b> object.

Before using this method, you must call both the 
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926942">Reset</a> method to size the array and the 
<a href="https://msdn.microsoft.com/5da07c09-9213-4604-b058-5e69df646b09">SetNameEntry</a> method to set each array element.


## -parameters




### -param pstrBinary






#### - pbstrBinary [out]

A pointer to a <b>BSTR</b> that receives the ASN.1-encoded alternate name extension. When done, call <a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> to free <i>pbstrBinary</i>.


## -returns



<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is the ASN.1-encoded alternate name array.




## -see-also




<a href="https://msdn.microsoft.com/e0ecfcb0-f2ca-4e1c-a054-c83c03d55465">ICertEncodeAltName</a>



<a href="https://msdn.microsoft.com/0507d3a5-b8c3-4f2e-996f-e1e32957f475">ICertEncodeAltName::Decode</a>



<a href="https://msdn.microsoft.com/99aa43fe-534b-4696-8bfc-7049b16be1cf">ICertEncodeAltName::Reset</a>



<a href="https://msdn.microsoft.com/5da07c09-9213-4604-b058-5e69df646b09">ICertEncodeAltName::SetNameEntry</a>
 

 

