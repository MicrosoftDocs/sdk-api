---
UID: NF:certenc.ICertEncodeCRLDistInfo.GetNameCount
title: ICertEncodeCRLDistInfo::GetNameCount
author: windows-sdk-content
description: Returns the number of names in a certificate revocation list (CRL) distribution point.
old-location: security\icertencodecrldistinfo_getnamecount.htm
tech.root: seccrypto
ms.assetid: 64102b89-defe-4f26-b6b2-8c3903e08347
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: CCertEncodeCRLDistInfo object [Security],GetNameCount method, GetNameCount, GetNameCount method [Security], GetNameCount method [Security],CCertEncodeCRLDistInfo object, GetNameCount method [Security],ICertEncodeCRLDistInfo interface, ICertEncodeCRLDistInfo interface [Security],GetNameCount method, ICertEncodeCRLDistInfo.GetNameCount, ICertEncodeCRLDistInfo::GetNameCount, _certsrv_icertencodecrldistinfo_getnamecount, certenc/ICertEncodeCRLDistInfo::GetNameCount, security.icertencodecrldistinfo_getnamecount
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
 - ICertEncodeCRLDistInfo.GetNameCount
 - CCertEncodeCRLDistInfo.GetNameCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertEncodeCRLDistInfo::GetNameCount


## -description


The <b>GetNameCount</b> method returns the number of names in a <a href="https://msdn.microsoft.com/en-us/library/ms721572(v=VS.85).aspx">certificate revocation list</a> (CRL) distribution point.


## -parameters




### -param DistPointIndex [in]

Specifies the index of the distribution point for which to get the name count.


### -param pNameCount [out]

A pointer to a <b>Long</b> that will represent the number of name values contained in the CRL distribution point.


## -returns



<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/en-us/library/Aa378137(v=VS.85).aspx">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is the number of names in the CRL distribution point.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa383911(v=VS.85).aspx">ICertEncodeCRLDistInfo</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa383936(v=VS.85).aspx">ICertEncodeCRLDistInfo::GetDistPointCount</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa383945(v=VS.85).aspx">ICertEncodeCRLDistInfo::GetName</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa383982(v=VS.85).aspx">ICertEncodeCRLDistInfo::SetNameCount</a>
 

 

