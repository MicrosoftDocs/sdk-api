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

# ICertEncodeLongArray::Encode


## -description


The <b>Encode</b> method returns an ASN.1-encoded string of the <b>LONG</b> array stored in this object.

Use the <a href="https://msdn.microsoft.com/b0ff8e1a-c4b2-48ac-be95-228638d00e6d">Decode</a> method to decode the encoded string into an <b>CertEncodeLongArray</b> object.

Before calling the <b>Encode</b> method, you must call the 
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926942">Reset</a> method to size the array and the 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff597642">SetValue</a> method to set each <b>LONG</b> value in the array.


## -parameters




### -param pstrBinary






#### - pbstrBinary [out]

A pointer to a <b>BSTR</b> that will contain the encoded <b>LONG</b> array. When you have finished using the <b>BSTR</b>, free it by calling the <a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> function.


## -returns



<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

<h3>VB</h3>
The return value is the ASN.1-encoded <b>LONG</b> array.




## -see-also




<a href="https://msdn.microsoft.com/e8555282-6c09-4f23-830e-358bc73287ee">ICertEncodeLongArray</a>



<a href="https://msdn.microsoft.com/b0ff8e1a-c4b2-48ac-be95-228638d00e6d">ICertEncodeLongArray::Decode</a>



<a href="https://msdn.microsoft.com/4b5821e0-c81a-47b7-98b0-2a293967d8f6">ICertEncodeLongArray::Reset</a>



<a href="https://msdn.microsoft.com/021b2539-3226-4893-af76-9b7b1637e12e">ICertEncodeLongArray::SetValue</a>
 

 

