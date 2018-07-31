---
UID: NS:wincrypt._CMC_PEND_INFO
title: "_CMC_PEND_INFO"
author: windows-sdk-content
description: A possible member of a CMC_STATUS_INFO structure.
old-location: security\cmc_pend_info.htm
old-project: SecCrypto
ms.assetid: ac3dcd19-caed-4453-bac7-55ffa3a02f54
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: "*PCMC_PEND_INFO, CMC_PEND_INFO, CMC_PEND_INFO structure [Security], PCMC_PEND_INFO, PCMC_PEND_INFO structure pointer [Security], _CMC_PEND_INFO, _crypto2_cmc_pend_info, security.cmc_pend_info, wincrypt/CMC_PEND_INFO, wincrypt/PCMC_PEND_INFO"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: CMC_PEND_INFO, *PCMC_PEND_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - CMC_PEND_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _CMC_PEND_INFO structure


## -description


The <b>CMC_PEND_INFO</b> structure is a possible member of a 
<a href="https://msdn.microsoft.com/008f6de4-bad2-4c63-ba64-8d42ae71d50a">CMC_STATUS_INFO</a> structure.


## -struct-fields




### -field PendToken

A <a href="https://msdn.microsoft.com/2e570727-7da0-4e17-bf5d-6fe0e6aef65b">BLOB</a> that contains the pending request information.


### -field PendTime

<b>FILETIME</b> containing the request.

