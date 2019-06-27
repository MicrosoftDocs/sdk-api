---
UID: NS:wincrypt._CERT_NAME_CONSTRAINTS_INFO
title: CERT_NAME_CONSTRAINTS_INFO (wincrypt.h)
author: windows-sdk-content
description: The CERT_NAME_CONSTRAINTS_INFO structure contains information about certificates that are specifically permitted or excluded from trust.
old-location: security\cert_name_constraints_info.htm
tech.root: SecCrypto
ms.assetid: 16a57c4b-905f-40c0-b298-71f0534bfa5a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PCERT_NAME_CONSTRAINTS_INFO, CERT_NAME_CONSTRAINTS_INFO, CERT_NAME_CONSTRAINTS_INFO structure [Security], PCERT_NAME_CONSTRAINTS_INFO, PCERT_NAME_CONSTRAINTS_INFO structure pointer [Security], _crypto2_cert_name_constraints_info, security.cert_name_constraints_info, wincrypt/CERT_NAME_CONSTRAINTS_INFO, wincrypt/PCERT_NAME_CONSTRAINTS_INFO"
ms.topic: struct
f1_keywords: 
 - "wincrypt/CERT_NAME_CONSTRAINTS_INFO"
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - CERT_NAME_CONSTRAINTS_INFO
product: Windows
targetos: Windows
req.typenames: CERT_NAME_CONSTRAINTS_INFO, *PCERT_NAME_CONSTRAINTS_INFO
req.redist: 
ms.custom: 19H1
---

# CERT_NAME_CONSTRAINTS_INFO structure


## -description


The <b>CERT_NAME_CONSTRAINTS_INFO</b> structure contains information about certificates that are specifically permitted or excluded from trust.


## -struct-fields




### -field cPermittedSubtree

<b>DWORD</b> indicating the number of subtrees in the <b>rgPermittedSubtree</b> array.


### -field rgPermittedSubtree

Array of 
<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/ns-wincrypt-_cert_general_subtree">CERT_GENERAL_SUBTREE</a> structures, each identifying a permitted certificate name.


### -field cExcludedSubtree

<b>DWORD</b> indicating the number of subtrees in the <b>rgExcludedSubtree</b> array.


### -field rgExcludedSubtree

Array of <a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/ns-wincrypt-_cert_general_subtree">CERT_GENERAL_SUBTREE</a> structures, each identifying an excluded certificate name.

