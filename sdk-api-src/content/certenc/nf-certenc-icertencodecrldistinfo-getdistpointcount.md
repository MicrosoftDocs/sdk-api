---
UID: NF:certenc.ICertEncodeCRLDistInfo.GetDistPointCount
title: ICertEncodeCRLDistInfo::GetDistPointCount
author: windows-sdk-content
description: Returns the number of certificate revocation list (CRL) distribution points in a CRL distribution information array.
old-location: security\icertencodecrldistinfo_getdistpointcount.htm
old-project: SecCrypto
ms.assetid: 8c7d0d14-e755-4223-8cd5-0ebc784960cf
ms.author: windowssdkdev
ms.date: 08/15/2018
ms.keywords: CCertEncodeCRLDistInfo object [Security],GetDistPointCount method, GetDistPointCount, GetDistPointCount method [Security], GetDistPointCount method [Security],CCertEncodeCRLDistInfo object, GetDistPointCount method [Security],ICertEncodeCRLDistInfo interface, ICertEncodeCRLDistInfo interface [Security],GetDistPointCount method, ICertEncodeCRLDistInfo.GetDistPointCount, ICertEncodeCRLDistInfo::GetDistPointCount, _certsrv_icertencodecrldistinfo_getdistpointcount, certenc/ICertEncodeCRLDistInfo::GetDistPointCount, security.icertencodecrldistinfo_getdistpointcount
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: certenc.h
req.include-header: Certsrv.h
req.redist: 
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
 - ICertEncodeCRLDistInfo.GetDistPointCount
 - CCertEncodeCRLDistInfo.GetDistPointCount
product: Windows
targetos: Windows
req.lib: Certidl.lib
req.dll: Certenc.dll
req.irql: 
---

# ICertEncodeCRLDistInfo::GetDistPointCount


## -description


The <b>GetDistPointCount</b> method returns the number of <a href="https://msdn.microsoft.com/en-us/library/ms721572(v=VS.85).aspx">certificate revocation list</a> (CRL) distribution points in a CRL distribution information array.


## -parameters




### -param pDistPointCount [out]

A pointer to a <b>LONG</b> that will represent the number of CRL distribution points in the array.


## -returns



<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/en-us/library/Aa378137(v=VS.85).aspx">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is the number of CRL distribution points in the array. 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa383911(v=VS.85).aspx">ICertEncodeCRLDistInfo</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa383963(v=VS.85).aspx">ICertEncodeCRLDistInfo::GetNameCount</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa383969(v=VS.85).aspx">ICertEncodeCRLDistInfo::Reset</a>
 

 

