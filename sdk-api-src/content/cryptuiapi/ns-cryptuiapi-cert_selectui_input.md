---
UID: NS:cryptuiapi.CERT_SELECTUI_INPUT
title: CERT_SELECTUI_INPUT
author: windows-sdk-content
description: Used by the CertSelectionGetSerializedBlob function to serialize the certificates contained in a store or an array of certificate chains. The returned serialized BLOB can be passed to the CredUIPromptForWindowsCredentials function.
old-location: security\cert_selectui_input.htm
tech.root: seccrypto
ms.assetid: 8953cddd-86b6-4781-8dca-b5fd3d298bc8
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: "*PCERT_SELECTUI_INPUT, CERT_SELECTUI_INPUT, CERT_SELECTUI_INPUT structure [Security], PCERT_SELECTUI_INPUT, PCERT_SELECTUI_INPUT structure pointer [Security], cryptuiapi/CERT_SELECTUI_INPUT, cryptuiapi/PCERT_SELECTUI_INPUT, security.cert_selectui_input"
ms.prod: windows
ms.technology: windows-sdk
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
---

# CERT_SELECTUI_INPUT structure


## -description


The <b>CERT_SELECTUI_INPUT</b> structure is used by the <a href="https://msdn.microsoft.com/en-us/library/Ff394769(v=VS.85).aspx">CertSelectionGetSerializedBlob</a> function to serialize the certificates contained in a store or an array of certificate chains. The returned serialized <a href="https://msdn.microsoft.com/en-us/library/ms721569(v=VS.85).aspx">BLOB</a> can be passed to the <a href="https://msdn.microsoft.com/en-us/library/Aa375178(v=VS.85).aspx">CredUIPromptForWindowsCredentials</a> function.


## -struct-fields




### -field hStore

The  handle of a certificate store created by the caller. The store contains the set of  application preselected certificates. 


### -field prgpChain

An array of pointers to <a href="https://msdn.microsoft.com/en-us/library/Aa377182(v=VS.85).aspx">CERT_CHAIN_CONTEXT</a> structures. Applications provision this array by preselecting certificate chains using the <a href="https://msdn.microsoft.com/en-us/library/Dd433797(v=VS.85).aspx">CertSelectCertificateChains</a> function.


### -field cChain

The number of <a href="https://msdn.microsoft.com/en-us/library/Aa377182(v=VS.85).aspx">CERT_CHAIN_CONTEXT</a> structures that are in the array pointed to by the <b>prgpChain</b> member.

