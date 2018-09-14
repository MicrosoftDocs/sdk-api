---
UID: NF:wincrypt.CertVerifyCRLTimeValidity
title: CertVerifyCRLTimeValidity function
author: windows-sdk-content
description: The CertVerifyCRLTimeValidity function verifies the time validity of a CRL.
old-location: security\certverifycrltimevalidity.htm
tech.root: seccrypto
ms.assetid: ff321fe8-df45-4a1d-b626-055fb0696438
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: CertVerifyCRLTimeValidity, CertVerifyCRLTimeValidity function [Security], _crypto2_certverifycrltimevalidity, security.certverifycrltimevalidity, wincrypt/CertVerifyCRLTimeValidity
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wincrypt.h
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
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Crypt32.dll
api_name:
 - CertVerifyCRLTimeValidity
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CertVerifyCRLTimeValidity function


## -description


The <b>CertVerifyCRLTimeValidity</b> function verifies the time validity of a CRL.


## -parameters




### -param pTimeToVerify [in]

A pointer to <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure containing the time to be used in the verification. If set to <b>NULL</b>, the current time is used.


### -param pCrlInfo [in]

A pointer to a 
<a href="https://msdn.microsoft.com/06a28de3-dd7c-4efe-9baa-20aac69d63f3">CRL_INFO</a> structure containing the CRL for which the time is to be verified.


## -returns



Returns a minus one (–1) if the comparison time is before the <b>ThisUpdate</b> member of the <a href="https://msdn.microsoft.com/06a28de3-dd7c-4efe-9baa-20aac69d63f3">CRL_INFO</a> pointed to by <i>pCrlInfo</i>. Returns a plus one (+1) if the comparison time is after the <b>NextUpdate</b> time. Returns zero for valid time for the CRL.




## -see-also




<a href="https://msdn.microsoft.com/a46ac5b5-bc44-4857-a7fb-4f35d438e3f7">CertVerifyCRLRevocation</a>



<a href="https://msdn.microsoft.com/9ccf9230-e998-4f82-9db0-6cbaa1c36850">CertVerifyTimeValidity</a>



<a href="https://msdn.microsoft.com/dc73a21d-5b55-45c4-80d2-220508d9f762">CertVerifyValidityNesting</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa380252(v=VS.85).aspx">Data Management Functions</a>
 

 

