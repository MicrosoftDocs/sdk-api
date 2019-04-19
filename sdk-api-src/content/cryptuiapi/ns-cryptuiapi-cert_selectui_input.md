---
UID: NS:cryptuiapi.__unnamed_struct_0
title: CERT_SELECTUI_INPUT (cryptuiapi.h)
author: windows-sdk-content
description: Used by the CertSelectionGetSerializedBlob function to serialize the certificates contained in a store or an array of certificate chains. The returned serialized BLOB can be passed to the CredUIPromptForWindowsCredentials function.
old-location: security\cert_selectui_input.htm
tech.root: SecCrypto
ms.assetid: 8953cddd-86b6-4781-8dca-b5fd3d298bc8
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PCERT_SELECTUI_INPUT, CERT_SELECTUI_INPUT, CERT_SELECTUI_INPUT structure [Security], PCERT_SELECTUI_INPUT, PCERT_SELECTUI_INPUT structure pointer [Security], cryptuiapi/CERT_SELECTUI_INPUT, cryptuiapi/PCERT_SELECTUI_INPUT, security.cert_selectui_input"
ms.topic: struct
req.header: cryptuiapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - Cryptuiapi.h
api_name:
 - CERT_SELECTUI_INPUT
product: Windows
targetos: Windows
req.typenames: CERT_SELECTUI_INPUT, *PCERT_SELECTUI_INPUT
req.redist: 
ms.custom: 19H1
---

# CERT_SELECTUI_INPUT structure


## -description


The <b>CERT_SELECTUI_INPUT</b> structure is used by the <a href="https://msdn.microsoft.com/6c3240f7-5121-401d-a4d4-df3055cb301a">CertSelectionGetSerializedBlob</a> function to serialize the certificates contained in a store or an array of certificate chains. The returned serialized <a href="https://msdn.microsoft.com/2e570727-7da0-4e17-bf5d-6fe0e6aef65b">BLOB</a> can be passed to the <a href="https://msdn.microsoft.com/946ac279-d30a-4a6c-a76d-d93597121427">CredUIPromptForWindowsCredentials</a> function.


## -struct-fields




### -field hStore

The  handle of a certificate store created by the caller. The store contains the set of  application preselected certificates. 


### -field prgpChain

An array of pointers to <a href="https://msdn.microsoft.com/609311f4-9cd6-4945-9f93-7266b3fc4a74">CERT_CHAIN_CONTEXT</a> structures. Applications provision this array by preselecting certificate chains using the <a href="https://msdn.microsoft.com/b740772b-d25b-4b3d-9acb-03f7018750d6">CertSelectCertificateChains</a> function.


### -field cChain

The number of <a href="https://msdn.microsoft.com/609311f4-9cd6-4945-9f93-7266b3fc4a74">CERT_CHAIN_CONTEXT</a> structures that are in the array pointed to by the <b>prgpChain</b> member.

