---
UID: NF:certenc.ICertEncodeCRLDistInfo.GetName
title: ICertEncodeCRLDistInfo::GetName method
author: windows-driver-content
description: Returns the name at a specified index of a certificate revocation list (CRL) distribution information point.
old-location: security\icertencodecrldistinfo_getname.htm
old-project: SecCrypto
ms.assetid: a564af61-fb5e-46b7-a818-333b4d5e2f25
ms.author: windowsdriverdev
ms.date: 4/18/2018
ms.keywords: CCertEncodeCRLDistInfo object [Security], GetName method, GetName method [Security], GetName method [Security], CCertEncodeCRLDistInfo object, GetName method [Security], ICertEncodeCRLDistInfo interface, GetName,ICertEncodeCRLDistInfo.GetName, ICertEncodeCRLDistInfo, ICertEncodeCRLDistInfo interface [Security], GetName method, ICertEncodeCRLDistInfo::GetName, _certsrv_icertencodecrldistinfo_getname, certenc/ICertEncodeCRLDistInfo::GetName, security.icertencodecrldistinfo_getname
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: X509EnrollmentAuthFlags
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Certenc.dll
api_name:
-	ICertEncodeCRLDistInfo.GetName
-	CCertEncodeCRLDistInfo.GetName
product: Windows
targetos: Windows
req.lib: Certidl.lib
req.dll: Certenc.dll
req.irql: 
---

# ICertEncodeCRLDistInfo::GetName method


## -description


The <b>GetName</b> method returns the name at a specified index of a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate revocation list</a> (CRL) distribution information point.


## -parameters




### -param DistPointIndex [in]

Specifies the index of the distribution point for which to get a name. The first value is at index zero.


### -param NameIndex [in]

Specifies the index of the name entry to get. The first value is at index zero.


### -param pstrName






#### - pbstrName [out]

A pointer to a <b>BSTR</b> that represents the name value. When you have finished using the <b>BSTR</b>, free it by calling the <a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> function.


## -returns



<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is the name at the specified index of the specified distribution point. The return value is a <a href="https://msdn.microsoft.com/264f6cb6-36c6-4cdb-b7bb-a5dbd332adcb">Unicode</a> string.




## -see-also




<a href="https://msdn.microsoft.com/e9c0053f-263f-4d7b-9356-bc33af989dbe">ICertEncodeCRLDistInfo</a>



<a href="https://msdn.microsoft.com/64102b89-defe-4f26-b6b2-8c3903e08347">ICertEncodeCRLDistInfo::GetNameCount</a>



<a href="https://msdn.microsoft.com/fe33265a-8c75-4e16-8178-3569cf30d8e4">ICertEncodeCRLDistInfo::SetNameEntry</a>
 

 

