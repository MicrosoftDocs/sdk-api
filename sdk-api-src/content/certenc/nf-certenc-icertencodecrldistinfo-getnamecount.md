---
UID: NF:certenc.ICertEncodeCRLDistInfo.GetNameCount
title: ICertEncodeCRLDistInfo::GetNameCount
author: windows-sdk-content
description: Returns the number of names in a certificate revocation list (CRL) distribution point.
old-location: security\icertencodecrldistinfo_getnamecount.htm
old-project: SecCrypto
ms.assetid: 64102b89-defe-4f26-b6b2-8c3903e08347
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: CCertEncodeCRLDistInfo object [Security],GetNameCount method, GetNameCount, GetNameCount method [Security], GetNameCount method [Security],CCertEncodeCRLDistInfo object, GetNameCount method [Security],ICertEncodeCRLDistInfo interface, ICertEncodeCRLDistInfo interface [Security],GetNameCount method, ICertEncodeCRLDistInfo.GetNameCount, ICertEncodeCRLDistInfo::GetNameCount, _certsrv_icertencodecrldistinfo_getnamecount, certenc/ICertEncodeCRLDistInfo::GetNameCount, security.icertencodecrldistinfo_getnamecount
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: X509EnrollmentAuthFlags
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certenc.dll
api_name:
 - ICertEncodeCRLDistInfo.GetNameCount
 - CCertEncodeCRLDistInfo.GetNameCount
product: Windows
targetos: Windows
req.lib: Certidl.lib
req.dll: Certenc.dll
req.irql: 
---

# ICertEncodeCRLDistInfo::GetNameCount


## -description


The <b>GetNameCount</b> method returns the number of names in a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate revocation list</a> (CRL) distribution point.


## -parameters




### -param DistPointIndex [in]

Specifies the index of the distribution point for which to get the name count.


### -param pNameCount [out]

A pointer to a <b>Long</b> that will represent the number of name values contained in the CRL distribution point.


## -returns



<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is the number of names in the CRL distribution point.




## -see-also




<a href="https://msdn.microsoft.com/e9c0053f-263f-4d7b-9356-bc33af989dbe">ICertEncodeCRLDistInfo</a>



<a href="https://msdn.microsoft.com/8c7d0d14-e755-4223-8cd5-0ebc784960cf">ICertEncodeCRLDistInfo::GetDistPointCount</a>



<a href="https://msdn.microsoft.com/a564af61-fb5e-46b7-a818-333b4d5e2f25">ICertEncodeCRLDistInfo::GetName</a>



<a href="https://msdn.microsoft.com/ce27adfd-e21a-4e8d-882e-72041f97958a">ICertEncodeCRLDistInfo::SetNameCount</a>
 

 

