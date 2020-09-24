---
UID: NS:wincrypt._CERT_QC_STATEMENTS_EXT_INFO
title: CERT_QC_STATEMENTS_EXT_INFO (wincrypt.h)
description: Contains a sequence of one or more statements that make up the Qualified Certificate (QC) statements extension for a QC.
helpviewer_keywords: ["*PCERT_QC_STATEMENTS_EXT_INFO","CERT_QC_STATEMENTS_EXT_INFO","CERT_QC_STATEMENTS_EXT_INFO structure [Security]","PCERT_QC_STATEMENTS_EXT_INFO","PCERT_QC_STATEMENTS_EXT_INFO structure pointer [Security]","security.cert_qc_statements_ext_info","wincrypt/CERT_QC_STATEMENTS_EXT_INFO","wincrypt/PCERT_QC_STATEMENTS_EXT_INFO"]
old-location: security\cert_qc_statements_ext_info.htm
tech.root: security
ms.assetid: 788b3848-8d38-4e8f-9fdb-452767fbac61
ms.date: 12/05/2018
ms.keywords: '*PCERT_QC_STATEMENTS_EXT_INFO, CERT_QC_STATEMENTS_EXT_INFO, CERT_QC_STATEMENTS_EXT_INFO structure [Security], PCERT_QC_STATEMENTS_EXT_INFO, PCERT_QC_STATEMENTS_EXT_INFO structure pointer [Security], security.cert_qc_statements_ext_info, wincrypt/CERT_QC_STATEMENTS_EXT_INFO, wincrypt/PCERT_QC_STATEMENTS_EXT_INFO'
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: CERT_QC_STATEMENTS_EXT_INFO, *PCERT_QC_STATEMENTS_EXT_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CERT_QC_STATEMENTS_EXT_INFO
 - wincrypt/_CERT_QC_STATEMENTS_EXT_INFO
 - PCERT_QC_STATEMENTS_EXT_INFO
 - wincrypt/PCERT_QC_STATEMENTS_EXT_INFO
 - CERT_QC_STATEMENTS_EXT_INFO
 - wincrypt/CERT_QC_STATEMENTS_EXT_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - CERT_QC_STATEMENTS_EXT_INFO
---

# CERT_QC_STATEMENTS_EXT_INFO structure


## -description

The <b>CERT_QC_STATEMENTS_EXT_INFO</b> structure contains a sequence of one or more statements that make up the Qualified Certificate (QC) statements extension for a QC.

## -struct-fields

### -field cStatement

A value that represents the size, in bytes, of the <b>rgStatement</b> array.

### -field rgStatement

An array of <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_qc_statement">CERT_QC_STATEMENT</a> structures that contains the sequence of statements that make up the QC statements extension.

## -see-also

<a href="https://www.ietf.org/rfc/rfc3280.txt">RFC 3280</a>



<a href="https://www.ietf.org/rfc/rfc3739.txt">RFC 3739</a>