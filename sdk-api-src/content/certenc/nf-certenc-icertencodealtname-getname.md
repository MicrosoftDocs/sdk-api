---
UID: NF:certenc.ICertEncodeAltName.GetName
title: ICertEncodeAltName::GetName
author: windows-sdk-content
description: Returns the specified name from the alternate name array.
old-location: security\icertencodealtname_getname.htm
tech.root: SecCrypto
ms.assetid: 25a3f36b-1c09-4b2e-84b7-a725d366fd77
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CCertEncodeAltName object [Security],GetName method, GetName, GetName method [Security], GetName method [Security],CCertEncodeAltName object, GetName method [Security],ICertEncodeAltName interface, ICertEncodeAltName interface [Security],GetName method, ICertEncodeAltName.GetName, ICertEncodeAltName::GetName, _certsrv_icertencodealtname_getname, certenc/ICertEncodeAltName::GetName, security.icertencodealtname_getname
ms.topic: method
req.header: certenc.h
req.include-header: Certsrv.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Certidl.lib
req.dll: Certenc.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certenc.dll
api_name:
 - ICertEncodeAltName.GetName
 - CCertEncodeAltName.GetName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertEncodeAltName::GetName


## -description


The <b>GetName</b> method returns the specified name from the alternate name array.


## -parameters




### -param NameIndex [in]

A zero-based index that specifies the index of the alternate name entry to retrieve.  

To retrieve the <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID) of a CERT_ALT_NAME_OTHER_NAME name, combine the index value with EAN_NAMEOBJECTID (defined as 0x80000000) with a bitwise-<b>OR</b> operation. Otherwise, the binary value is retrieved. To determine the type of name, call the <a href="https://msdn.microsoft.com/3b21fbc7-cba1-49b1-bad6-232f717e3056">ICertEncodeAltName::GetNameChoice</a> method.


### -param pstrName [out]

A pointer to a <b>BSTR</b> that receives the alternate name. When you have finished using the <b>BSTR</b>, free it by calling the <a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a> function.


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
 

 

