---
UID: NS:wintrust.WINTRUST_SGNR_INFO_
title: WINTRUST_SGNR_INFO_
author: windows-sdk-content
description: Used when calling WinVerifyTrust to verify a CMSG_SIGNER_INFO structure.
old-location: security\wintrust_sgnr_info.htm
old-project: SecCrypto
ms.assetid: 04e62bfa-efe4-428a-ae6b-58c2377fd5ba
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: "*PWINTRUST_SGNR_INFO, PWINTRUST_SGNR_INFO, PWINTRUST_SGNR_INFO structure pointer [Security], WINTRUST_SGNR_INFO, WINTRUST_SGNR_INFO structure [Security], WINTRUST_SGNR_INFO_, _win32_wintrust_sgnr_info, security.wintrust_sgnr_info, wintrust/PWINTRUST_SGNR_INFO, wintrust/WINTRUST_SGNR_INFO"
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
req.typenames: WINTRUST_SGNR_INFO, *PWINTRUST_SGNR_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wintrust.h
api_name:
 - WINTRUST_SGNR_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WINTRUST_SGNR_INFO_ structure


## -description


<p class="CCE_Message">[The  <b>WINTRUST_SGNR_INFO</b> structure is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>WINTRUST_SGNR_INFO</b> structure is used when calling 
<a href="https://msdn.microsoft.com/b7efac6a-ac9f-477a-aada-63fe32208e6f">WinVerifyTrust</a> to verify a 
<a href="https://msdn.microsoft.com/eae631d2-5e5f-4964-b079-9692831b34fc">CMSG_SIGNER_INFO</a> structure.


## -struct-fields




### -field cbStruct

Count of bytes in this structure.


### -field pcwszDisplayName

String with the name representing the signer to be checked.


### -field psSignerInfo

A pointer to a 
<a href="https://msdn.microsoft.com/eae631d2-5e5f-4964-b079-9692831b34fc">CMSG_SIGNER_INFO</a> structure that includes the <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">signature</a> to be verified.


### -field chStores

Number of store handles in <b>pahStores</b>.


### -field pahStores

An array of open <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate stores</a> to be added to the list of stores that the policy provider uses to find certificates while building a trust chain.

