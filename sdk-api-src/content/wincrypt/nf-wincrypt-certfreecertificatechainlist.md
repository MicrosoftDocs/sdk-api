---
UID: NF:wincrypt.CertFreeCertificateChainList
title: CertFreeCertificateChainList function
author: windows-sdk-content
description: Frees the array of pointers to chain contexts.
old-location: security\certfreecertificatechainlist.htm
old-project: seccrypto
ms.assetid: a53b02ca-bc3f-43fd-8c90-2f646d550182
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: CertFreeCertificateChainList, CertFreeCertificateChainList function [Security], security.certfreecertificatechainlist, wincrypt/CertFreeCertificateChainList
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
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
req.typenames: USERNAME_TARGET_CREDENTIAL_INFO, *PUSERNAME_TARGET_CREDENTIAL_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Crypt32.dll
api_name:
 - CertFreeCertificateChainList
product: Windows
targetos: Windows
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# CertFreeCertificateChainList function


## -description


The <b>CertFreeCertificateChainList</b> function frees the array of pointers to chain contexts.


## -parameters




### -param prgpSelection [in]

A pointer to a <a href="https://msdn.microsoft.com/609311f4-9cd6-4945-9f93-7266b3fc4a74">PCCERT_CHAIN_CONTEXT</a> structure returned by the <a href="https://msdn.microsoft.com/b740772b-d25b-4b3d-9acb-03f7018750d6">CertSelectCertificateChains</a> function.


## -returns



This function does not return a value.




## -remarks



 Before calling the <b>CertFreeCertificateChainList</b> function, you must call the  <a href="https://msdn.microsoft.com/5ba181c2-6936-4848-a571-2bb58f46f081">CertFreeCertificateChain</a> function on each chain context within the array pointed to by the <i>prgpSelection</i> parameter.  



