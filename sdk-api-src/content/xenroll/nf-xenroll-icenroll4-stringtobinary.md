---
UID: NF:xenroll.ICEnroll4.stringToBinary
title: ICEnroll4::stringToBinary (xenroll.h)
author: windows-sdk-content
description: Converts an encoded string to a binary data BLOB. This method was first defined in the ICEnroll4 interface.
old-location: security\icenroll4_stringtobinary.htm
tech.root: SecCrypto
ms.assetid: abcc395f-f989-4098-818a-160e427b1da0
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CEnroll object [Security],stringToBinary method, ICEnroll4 interface [Security],stringToBinary method, ICEnroll4.stringToBinary, ICEnroll4::stringToBinary, _xen_icenroll4_stringtobinary, security.icenroll4_stringtobinary, stringToBinary, stringToBinary method [Security], stringToBinary method [Security],CEnroll object, stringToBinary method [Security],ICEnroll4 interface, xenroll/ICEnroll4::stringToBinary
ms.topic: method
req.header: xenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.lib: Uuid.lib
req.dll: Xenroll.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Xenroll.dll
api_name:
 - ICEnroll4.stringToBinary
 - CEnroll.stringToBinary
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICEnroll4::stringToBinary


## -description


<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>stringToBinary</b> method converts an encoded string to a binary data <a href="https://msdn.microsoft.com/2e570727-7da0-4e17-bf5d-6fe0e6aef65b">BLOB</a>. This method was first defined in the <a href="https://msdn.microsoft.com/4e3e3792-aa41-46fe-bf75-26c2b8959f7a">ICEnroll4</a> interface.

The <b>stringToBinary</b> method calls the 
<a href="https://msdn.microsoft.com/13b6f5ef-174a-4254-8492-6e7dcc58945f">CryptStringToBinary</a> function.


## -parameters




### -param Flags [in]

A value passed to the <i>dwFlags</i> parameter of the <a href="https://msdn.microsoft.com/13b6f5ef-174a-4254-8492-6e7dcc58945f">CryptStringToBinary</a> function. For valid values, see 
<a href="https://msdn.microsoft.com/13b6f5ef-174a-4254-8492-6e7dcc58945f">CryptStringToBinary</a>.


### -param strEncoded [in]

An encoded string to be converted to a binary data <a href="https://msdn.microsoft.com/2e570727-7da0-4e17-bf5d-6fe0e6aef65b">BLOB</a>.


### -param pstrBinary [out]

A pointer to a  <b>BSTR</b> that receives the binary data. When you have finished using the <b>BSTR</b>, free it by calling the <a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a> function.


## -returns



<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see 
<a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is a string that contains the binary data.



