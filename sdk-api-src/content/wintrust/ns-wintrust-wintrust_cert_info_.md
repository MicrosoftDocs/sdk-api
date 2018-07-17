---
UID: NS:wintrust.WINTRUST_CERT_INFO_
title: WINTRUST_CERT_INFO_
author: windows-sdk-content
description: Used when calling WinVerifyTrust to verify a CERT_CONTEXT.
old-location: security\wintrust_cert_info.htm
old-project: SecCrypto
ms.assetid: 6522d1f0-3d96-4499-9220-23288122e0e6
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: "*PWINTRUST_CERT_INFO, PWINTRUST_CERT_INFO, PWINTRUST_CERT_INFO structure pointer [Security], WINTRUST_CERT_INFO, WINTRUST_CERT_INFO structure [Security], WINTRUST_CERT_INFO_, _win32_wintrust_cert_info, security.wintrust_cert_info, wintrust/PWINTRUST_CERT_INFO, wintrust/WINTRUST_CERT_INFO"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wintrust.h
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
tech.root: 
req.typenames: WINTRUST_CERT_INFO, *PWINTRUST_CERT_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wintrust.h
api_name:
 - WINTRUST_CERT_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WINTRUST_CERT_INFO_ structure


## -description


<p class="CCE_Message">[The  <b>WINTRUST_CERT_INFO</b> structure is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>WINTRUST_CERT_INFO</b> structure is used when calling 
<a href="https://msdn.microsoft.com/b7efac6a-ac9f-477a-aada-63fe32208e6f">WinVerifyTrust</a> to verify a 
<a href="https://msdn.microsoft.com/f0a3200e-6541-423d-a4a3-595a31026eea">CERT_CONTEXT</a>.


## -struct-fields




### -field cbStruct

Count of bytes in this structure.


### -field pcwszDisplayName

String with the name of the memory object pointed to by the <b>pbMem</b> member of the 
<a href="https://msdn.microsoft.com/8b13d355-4d24-4d8e-aae3-db16467999be">WINTRUST_BLOB_INFO</a> structure.


### -field psCertContext

A pointer to the 
<a href="https://msdn.microsoft.com/f0a3200e-6541-423d-a4a3-595a31026eea">CERT_CONTEXT</a> to be verified.


### -field chStores

The number of store handles in <b>pahStores</b>.


### -field pahStores

An array of open <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate stores</a> to add to the list of stores that the policy provider looks in to find certificates while building a trust chain.


### -field dwFlags

 


### -field psftVerifyAsOf

 



