---
UID: NF:mssip.CryptSIPCreateIndirectData
title: CryptSIPCreateIndirectData function (mssip.h)
description: Returns a SIP_INDIRECT_DATA structure that contains a hash of the supplied SIP_SUBJECTINFO structure, the digest algorithm, and an encoding attribute. The hash can be used as an indirect reference to the data.
helpviewer_keywords: ["CryptSIPCreateIndirectData","CryptSIPCreateIndirectData function [Security]","mssip/CryptSIPCreateIndirectData","security.cryptsipcreateindirectdata"]
old-location: security\cryptsipcreateindirectdata.htm
tech.root: security
ms.assetid: bb4ecc95-972f-415c-9722-59b00a27cddc
ms.date: 12/05/2018
ms.keywords: CryptSIPCreateIndirectData, CryptSIPCreateIndirectData function [Security], mssip/CryptSIPCreateIndirectData, security.cryptsipcreateindirectdata
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
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CryptSIPCreateIndirectData
 - mssip/CryptSIPCreateIndirectData
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Crypt32.dll
api_name:
 - CryptSIPCreateIndirectData
---

# CryptSIPCreateIndirectData function


## -description

The [SIP_SUBJECTINFO](/windows/desktop/api/mssip/ns-mssip-sip_subjectinfo) structure, the digest algorithm, and  an encoding attribute. The hash can be used as an indirect reference to the data.

## -parameters

### -param pSubjectInfo [in]

A pointer to a [SIP_SUBJECTINFO](/windows/desktop/api/mssip/ns-mssip-sip_subjectinfo) structure that contains the subject to which the indirect data reference will point.

### -param pcbIndirectData [in, out]

A pointer to a [SIP_INDIRECT_DATA](/windows/desktop/api/mssip/ns-mssip-sip_indirect_data) structure.

### -param pIndirectData [out]

A pointer to a [SIP_INDIRECT_DATA](/windows/desktop/api/mssip/ns-mssip-sip_indirect_data) structure to receive the catalog item.

## -returns

The return value is <b>TRUE</b> if the function succeeds; otherwise, <b>FALSE</b>.


If this function returns <b>FALSE</b>, additional error information can be obtained by calling the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function. <b>GetLastError</b> will return one of the following error codes.



<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BAD_FORMAT</b></dt>
</dl>
</td>
<td width="60%">
The file or data format is not correct for the specified <a href="/windows/desktop/SecGloss/s-gly">subject interface package</a> (SIP) type.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One or more of the parameters are not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
There was an error allocating memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_BAD_ALGID</b></dt>
</dl>
</td>
<td width="60%">
The specified algorithm is not supported by the SIP.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TRUST_E_SUBJECT_FORM_UNKNOWN</b></dt>
</dl>
</td>
<td width="60%">
The subject type is not recognized.

</td>
</tr>
</table>

## -remarks

If <i>pcbIndirectData</i> points to a <b>DWORD</b> and <i>pIndirectData</i> points to <b>NULL</b>, the size of the data will be returned
in <i>pcbIndirectData</i>.