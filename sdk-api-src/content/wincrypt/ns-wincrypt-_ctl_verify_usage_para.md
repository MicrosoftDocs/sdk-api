---
UID: NS:wincrypt._CTL_VERIFY_USAGE_PARA
title: "_CTL_VERIFY_USAGE_PARA"
author: windows-sdk-content
description: The CTL_VERIFY_USAGE_PARA structure contains parameters used by CertVerifyCTLUsage to establish the validity of a CTL's usage.
old-location: security\ctl_verify_usage_para.htm
tech.root: seccrypto
ms.assetid: bf9a3c81-f8c4-45a6-b045-8cbefebebbd3
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: "*PCTL_VERIFY_USAGE_PARA, CTL_VERIFY_USAGE_PARA, CTL_VERIFY_USAGE_PARA structure [Security], PCTL_VERIFY_USAGE_PARA, PCTL_VERIFY_USAGE_PARA structure pointer [Security], _CTL_VERIFY_USAGE_PARA, _crypto2_ctl_verify_usage_para, security.ctl_verify_usage_para, wincrypt/CTL_VERIFY_USAGE_PARA, wincrypt/PCTL_VERIFY_USAGE_PARA"
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
 - CTL_VERIFY_USAGE_PARA
product: Windows
targetos: Windows
req.typenames: CTL_VERIFY_USAGE_PARA, *PCTL_VERIFY_USAGE_PARA
req.redist: 
---

# _CTL_VERIFY_USAGE_PARA structure


## -description


The <b>CTL_VERIFY_USAGE_PARA</b> structure contains parameters used by 
<a href="https://msdn.microsoft.com/d87d8157-8e52-4198-bfd4-46d83d72eb13">CertVerifyCTLUsage</a> to establish the validity of a CTL's usage.


## -struct-fields




### -field cbSize

Size of this structure in bytes.


### -field ListIdentifier

<a href="https://msdn.microsoft.com/2e570727-7da0-4e17-bf5d-6fe0e6aef65b">BLOB</a> that specifies a <b>ListIdentifier</b> of a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">CTL</a> to be found or verified. Normally the <b>cbData</b> member of the <b>ListIdentifier</b> BLOB will be zero, indicating that a CTL with any <b>ListIdentifier</b> can be a match.

To match only CTLs with no <b>ListIdentifier</b>, the <b>cbData</b> member of the <b>ListIdentifier</b> BLOB is set to CTL_FIND_NO_LIST_ID_CBDATA.

If an issuer creates multiple CTLs for the same <b>SubjectUsage</b>, a <b>ListIdentifier</b> can distinguish among them.


### -field cCtlStore

The count of stores to be searched for a matching CTL.


### -field rghCtlStore

Array of handles of stores to be searched to find a matching CTL.


### -field cSignerStore

Count of stores to be searched for acceptable CTL signers.


### -field rghSignerStore

Array of handles of stores to be searched for acceptable CTL signers.


## -see-also




<a href="https://msdn.microsoft.com/d87d8157-8e52-4198-bfd4-46d83d72eb13">CertVerifyCTLUsage</a>
 

 

