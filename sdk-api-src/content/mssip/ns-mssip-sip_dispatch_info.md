---
UID: NS:mssip.SIP_DISPATCH_INFO_
title: SIP_DISPATCH_INFO (mssip.h)
description: Contains a set of function pointers assigned by the CryptSIPLoad function that your application uses to perform subject interface package (SIP) operations.
helpviewer_keywords: ["*LPSIP_DISPATCH_INFO","PSIP_DISPATCH_INFO","PSIP_DISPATCH_INFO structure pointer [Security]","SIP_DISPATCH_INFO","SIP_DISPATCH_INFO structure [Security]","mssip/PSIP_DISPATCH_INFO","mssip/SIP_DISPATCH_INFO","security.sip_dispatch_info"]
old-location: security\sip_dispatch_info.htm
tech.root: security
ms.assetid: d34b5081-0af8-4dcc-8133-a91d0603d419
ms.date: 12/05/2018
ms.keywords: '*LPSIP_DISPATCH_INFO, PSIP_DISPATCH_INFO, PSIP_DISPATCH_INFO structure pointer [Security], SIP_DISPATCH_INFO, SIP_DISPATCH_INFO structure [Security], mssip/PSIP_DISPATCH_INFO, mssip/SIP_DISPATCH_INFO, security.sip_dispatch_info'
req.header: mssip.h
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
targetos: Windows
req.typenames: SIP_DISPATCH_INFO, *LPSIP_DISPATCH_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SIP_DISPATCH_INFO_
 - mssip/SIP_DISPATCH_INFO_
 - LPSIP_DISPATCH_INFO
 - mssip/LPSIP_DISPATCH_INFO
 - SIP_DISPATCH_INFO
 - mssip/SIP_DISPATCH_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mssip.h
api_name:
 - SIP_DISPATCH_INFO
---

# SIP_DISPATCH_INFO structure


## -description

The <b>SIP_DISPATCH_INFO</b> structure contains a set of function pointers assigned by the <a href="/windows/desktop/api/mssip/nf-mssip-cryptsipload">CryptSIPLoad</a> function that your application uses to perform <a href="/windows/desktop/SecGloss/s-gly">subject interface package</a> (SIP) operations.

## -struct-fields

### -field cbSize

The size, in bytes, of this structure.

### -field hSIP

This member is reserved and must be set to <b>NULL</b>.

### -field pfGet

A pointer to the function that retrieves the signed data for the subject. The signature for this function pointer is described in <a href="/windows/desktop/api/mssip/nf-mssip-cryptsipgetsigneddatamsg">CryptSIPGetSignedDataMsg</a>.

### -field pfPut

A pointer to the function that stores the signed data for the subject. The signature for this function pointer is described in <a href="/windows/desktop/api/mssip/nf-mssip-cryptsipputsigneddatamsg">CryptSIPPutSignedDataMsg</a>.

### -field pfCreate

A pointer to the function that returns a [SIP_INDIRECT_DATA](/windows/desktop/api/mssip/ns-mssip-sip_indirect_data)  structure that contains the subject data. This structure contains the hash of the target. The signature for this function pointer is described in <a href="/windows/desktop/api/mssip/nf-mssip-cryptsipcreateindirectdata">CryptSIPCreateIndirectData</a>.

### -field pfVerify

A pointer to the function that verifies the [SIP_INDIRECT_DATA](/windows/desktop/api/mssip/ns-mssip-sip_indirect_data)  structure that contains the subject data. This structure contains the hash of the target. The signature for this function pointer is described in <a href="/windows/desktop/api/mssip/nf-mssip-cryptsipverifyindirectdata">CryptSIPVerifyIndirectData</a>.

### -field pfRemove

A pointer to the function that removes the signed data for the subject. The signature for this function pointer is described in <a href="/windows/desktop/api/mssip/nf-mssip-cryptsipremovesigneddatamsg">CryptSIPRemoveSignedDataMsg</a>.

## -remarks

Your application must initialize this structure to binary zeros and set <b>cbSize</b> to <code>sizeof(SIP_DISPATCH_INFO)</code> by calling the <a href="/cpp/c-runtime-library/reference/memset-wmemset">memset</a> function before calling the <a href="/windows/desktop/api/mssip/nf-mssip-cryptsipload">CryptSIPLoad</a> function. Your application can use the function pointers in the returned <b>SIP_DISPATCH_INFO</b> structure to perform the necessary SIP operations.   The function pointers can point to functions exported by third party SIPs.

## -see-also

<a href="/windows/desktop/api/mssip/nf-mssip-cryptsipcreateindirectdata">CryptSIPCreateIndirectData</a>



<a href="/windows/desktop/api/mssip/nf-mssip-cryptsipgetsigneddatamsg">CryptSIPGetSignedDataMsg</a>



<a href="/windows/desktop/api/mssip/nf-mssip-cryptsipputsigneddatamsg">CryptSIPPutSignedDataMsg</a>



<a href="/windows/desktop/api/mssip/nf-mssip-cryptsipremovesigneddatamsg">CryptSIPRemoveSignedDataMsg</a>



<a href="/windows/desktop/api/mssip/nf-mssip-cryptsipverifyindirectdata">CryptSIPVerifyIndirectData</a>