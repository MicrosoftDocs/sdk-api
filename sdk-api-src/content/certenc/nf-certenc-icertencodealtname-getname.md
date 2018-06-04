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

# ICertEncodeAltName::GetName


## -description


The <b>GetName</b> method returns the specified name from the alternate name array.


## -parameters




### -param NameIndex [in]

A zero-based index that specifies the index of the alternate name entry to retrieve.  

To retrieve the <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID) of a CERT_ALT_NAME_OTHER_NAME name, combine the index value with EAN_NAMEOBJECTID (defined as 0x80000000) with a bitwise-<b>OR</b> operation. Otherwise, the binary value is retrieved. To determine the type of name, call the <a href="https://msdn.microsoft.com/3b21fbc7-cba1-49b1-bad6-232f717e3056">ICertEncodeAltName::GetNameChoice</a> method.


### -param pstrName






#### - pbstrName [out]

A pointer to a <b>BSTR</b> that receives the alternate name. When you have finished using the <b>BSTR</b>, free it by calling the <a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> function.


## -returns



<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is the alternate name at the specified index. The return value is a <a href="https://msdn.microsoft.com/264f6cb6-36c6-4cdb-b7bb-a5dbd332adcb">Unicode</a> string.




## -see-also




<a href="https://msdn.microsoft.com/e0ecfcb0-f2ca-4e1c-a054-c83c03d55465">ICertEncodeAltName</a>



<a href="https://msdn.microsoft.com/3b21fbc7-cba1-49b1-bad6-232f717e3056">ICertEncodeAltName::GetNameChoice</a>



<a href="https://msdn.microsoft.com/5da07c09-9213-4604-b058-5e69df646b09">ICertEncodeAltName::SetNameEntry</a>
 

 

