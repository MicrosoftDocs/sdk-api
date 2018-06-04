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

# ICertEncodeDateArray::Encode


## -description


The <b>Encode</b> method returns an <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Abstract Syntax Notation One</a> (ASN.1)-encoded string of the date array stored in this object.

Use the <a href="https://msdn.microsoft.com/79937ef7-4b1a-4132-9ef4-23b2857c7fac">Decode</a> method to decode the encoded string into an <b>CertEncodeDateArray</b> object.

Before using this method, you must call both the 
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926942">Reset</a> method to size the array and the 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff597642">SetValue</a> method to set each array element.


## -parameters




### -param pstrBinary






#### - pbstrBinary [out]

A pointer to a <b>BSTR</b> that will contain the encoded <b>Date</b> array. When you have finished using the <b>BSTR</b>, free it by calling the <a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> function.


## -returns



<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is the ASN.1-encoded string that represents the <b>DATE</b> array.




## -see-also




<a href="https://msdn.microsoft.com/9973c49a-d886-4cc4-b75e-7ff46f56d51c">ICertEncodeDateArray</a>



<a href="https://msdn.microsoft.com/79937ef7-4b1a-4132-9ef4-23b2857c7fac">ICertEncodeDateArray::Decode</a>



<a href="https://msdn.microsoft.com/f09087aa-ae10-4a59-9b59-5f8b72254ce6">ICertEncodeDateArray::Reset</a>



<a href="https://msdn.microsoft.com/e05a7aa1-81ad-4564-a6a5-65b8ac816598">ICertEncodeDateArray::SetValue</a>
 

 

