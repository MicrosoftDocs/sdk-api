---
UID: NS:wincrypt._CERT_QC_STATEMENTS_EXT_INFO
title: "_CERT_QC_STATEMENTS_EXT_INFO"
author: windows-sdk-content
description: Contains a sequence of one or more statements that make up the Qualified Certificate (QC) statements extension for a QC.
old-location: security\cert_qc_statements_ext_info.htm
tech.root: seccrypto
ms.assetid: 788b3848-8d38-4e8f-9fdb-452767fbac61
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PCERT_QC_STATEMENTS_EXT_INFO, CERT_QC_STATEMENTS_EXT_INFO, CERT_QC_STATEMENTS_EXT_INFO structure [Security], PCERT_QC_STATEMENTS_EXT_INFO, PCERT_QC_STATEMENTS_EXT_INFO structure pointer [Security], _CERT_QC_STATEMENTS_EXT_INFO, security.cert_qc_statements_ext_info, wincrypt/CERT_QC_STATEMENTS_EXT_INFO, wincrypt/PCERT_QC_STATEMENTS_EXT_INFO"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - CERT_QC_STATEMENTS_EXT_INFO
product: Windows
targetos: Windows
req.typenames: CERT_QC_STATEMENTS_EXT_INFO, *PCERT_QC_STATEMENTS_EXT_INFO
req.redist: 
---

# _CERT_QC_STATEMENTS_EXT_INFO structure


## -description


The <b>CERT_QC_STATEMENTS_EXT_INFO</b> structure contains a sequence of one or more statements that make up the Qualified Certificate (QC) statements extension for a QC.


## -struct-fields




### -field cStatement

A value that represents the size, in bytes, of the <b>rgStatement</b> array.


### -field rgStatement

An array of <a href="https://msdn.microsoft.com/e163da81-d854-4f56-8eef-2788f1b566ba">CERT_QC_STATEMENT</a> structures that contains the sequence of statements that make up the QC statements extension.


## -see-also




<a href="http://go.microsoft.com/fwlink/p/?linkid=104367">RFC 3280</a>



<a href="http://go.microsoft.com/fwlink/p/?linkid=104368">RFC 3739</a>
 

 

