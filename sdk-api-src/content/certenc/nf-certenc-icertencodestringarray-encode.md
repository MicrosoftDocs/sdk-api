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

# ICertEncodeStringArray::Encode


## -description


The <b>Encode</b> method returns an ASN.1-encoded string of the string array stored in this object.

Use the <a href="https://msdn.microsoft.com/35799b54-2c04-4bb4-a227-d2902b2379ec">Decode</a> method to decode the encoded string into an <b>CertEncodeStringArray</b> object.

 Before using this method, you must call the <a href="https://msdn.microsoft.com/library/windows/hardware/dn926942">Reset</a> to size the array and the 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff597642">SetValue</a> method to set each string in the array.


## -parameters




### -param pstrBinary






#### - pbstrBinary [out]

A pointer to a <b>BSTR</b> that will contain the encoded string array. When you have finished using the <b>BSTR</b>, free it by calling the <a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> function.


## -returns



<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is the ASN.1-encoded string array.




## -see-also




<a href="https://msdn.microsoft.com/5515c25e-f788-4222-8f66-f5d86bd2a3a3">ICertEncodeStringArray</a>



<a href="https://msdn.microsoft.com/35799b54-2c04-4bb4-a227-d2902b2379ec">ICertEncodeStringArray::Decode</a>



<a href="https://msdn.microsoft.com/125524ae-236d-4507-9c00-76a016bf6c62">ICertEncodeStringArray::Reset</a>



<a href="https://msdn.microsoft.com/41e5c2b8-a0da-426a-b411-0bdc3fd7ecfe">ICertEncodeStringArray::SetValue</a>
 

 

