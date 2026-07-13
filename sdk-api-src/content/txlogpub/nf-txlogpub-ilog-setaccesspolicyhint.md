---
UID: NF:txlogpub.ILog.SetAccessPolicyHint
title: ILog::SetAccessPolicyHint (txlogpub.h)
description: Provides a hint to the implementation about the pattern in which records will be read.
helpviewer_keywords: ["ILog interface [COM]","SetAccessPolicyHint method","ILog.SetAccessPolicyHint","ILog::SetAccessPolicyHint","SetAccessPolicyHint","SetAccessPolicyHint method [COM]","SetAccessPolicyHint method [COM]","ILog interface","_com_ilog_setaccesspolicyhint","com.ilog_setaccesspolicyhint","txlogpub/ILog::SetAccessPolicyHint"]
old-location: com\ilog_setaccesspolicyhint.htm
tech.root: com
ms.assetid: a0a34300-e5de-4e47-9c61-389272283b61
ms.date: 12/05/2018
ms.keywords: ILog interface [COM],SetAccessPolicyHint method, ILog.SetAccessPolicyHint, ILog::SetAccessPolicyHint, SetAccessPolicyHint, SetAccessPolicyHint method [COM], SetAccessPolicyHint method [COM],ILog interface, _com_ilog_setaccesspolicyhint, com.ilog_setaccesspolicyhint, txlogpub/ILog::SetAccessPolicyHint
req.header: txlogpub.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Txlogpub.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ILog::SetAccessPolicyHint
 - txlogpub/ILog::SetAccessPolicyHint
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Txlogpub.h
api_name:
 - ILog.SetAccessPolicyHint
---

# ILog::SetAccessPolicyHint


## -description

Provides a hint to the implementation about the pattern in which records will be read.

## -parameters

### -param policy [in]

The pattern in which records will most often be read. For more information, see the <a href="/windows/desktop/api/txlogpub/ne-txlogpub-record_reading_policy">RECORD_READING_POLICY</a> enumeration.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Not all implementations of <a href="/windows/desktop/api/txlogpub/nn-txlogpub-ilog">ILog</a> will be optimized for reading records in a particular pattern. An implementation may choose to ignore this request and return S_OK.

## -see-also

<a href="/windows/desktop/api/txlogpub/nn-txlogpub-ilog">ILog</a>



<a href="/windows/desktop/api/txlogpub/ne-txlogpub-record_reading_policy">RECORD_READING_POLICY</a>