---
UID: NF:certenc.ICertEncodeCRLDistInfo.Reset
title: ICertEncodeCRLDistInfo::Reset
author: windows-sdk-content
description: Resets a certificate revocation list (CRL) distribution information array to a specified number of distribution point structures.
old-location: security\icertencodecrldistinfo_reset.htm
old-project: SecCrypto
ms.assetid: 899de888-918f-4202-a324-0e603eba2324
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: CCertEncodeCRLDistInfo object [Security],Reset method, ICertEncodeCRLDistInfo interface [Security],Reset method, ICertEncodeCRLDistInfo.Reset, ICertEncodeCRLDistInfo::Reset, Reset, Reset method [Security], Reset method [Security],CCertEncodeCRLDistInfo object, Reset method [Security],ICertEncodeCRLDistInfo interface, _certsrv_icertencodecrldistinfo_reset, certenc/ICertEncodeCRLDistInfo::Reset, security.icertencodecrldistinfo_reset
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
 - ICertEncodeCRLDistInfo.Reset
 - CCertEncodeCRLDistInfo.Reset
product: Windows
targetos: Windows
req.lib: Certidl.lib
req.dll: Certenc.dll
req.irql: 
---

# ICertEncodeCRLDistInfo::Reset


## -description


The <b>Reset</b> method resets a <a href="https://msdn.microsoft.com/en-us/library/ms721572(v=VS.85).aspx">certificate revocation list</a> (CRL) distribution information array to a specified number of distribution point structures.

 The values of all the elements in the array of structures are set to zero.


## -parameters




### -param DistPointCount [in]

Specifies the number of CRL distribution points in the CRL distribution information array.


## -returns



<h3>VB</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/en-us/library/Aa378137(v=VS.85).aspx">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa383911(v=VS.85).aspx">ICertEncodeCRLDistInfo</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa383936(v=VS.85).aspx">ICertEncodeCRLDistInfo::GetDistPointCount</a>
 

 

