---
UID: NF:mssip.CryptSIPCreateIndirectData
title: CryptSIPCreateIndirectData function
author: windows-sdk-content
description: Returns a SIP_INDIRECT_DATA structure that contains a hash of the supplied SIP_SUBJECTINFO structure, the digest algorithm, and an encoding attribute. The hash can be used as an indirect reference to the data.
old-location: security\cryptsipcreateindirectdata.htm
old-project: seccrypto
ms.assetid: bb4ecc95-972f-415c-9722-59b00a27cddc
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: CryptSIPCreateIndirectData, CryptSIPCreateIndirectData function [Security], mssip/CryptSIPCreateIndirectData, security.cryptsipcreateindirectdata
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: SimilarityFileId
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Crypt32.dll
api_name:
 - CryptSIPCreateIndirectData
product: Windows
targetos: Windows
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# CryptSIPCreateIndirectData function


## -description


The <b>CryptSIPCreateIndirectData</b> function returns a <a href="https://msdn.microsoft.com/d34b599b-fe49-47c4-bb52-73ee14d73253">SIP_INDIRECT_DATA</a> structure that contains  a <a href="https://msdn.microsoft.com/4165b820-30fc-477e-a690-81109f161323">hash</a> of  the supplied <a href="https://msdn.microsoft.com/6274cd08-d67f-410d-9303-3a42b7f1edc6">SIP_SUBJECTINFO</a> structure, the digest algorithm, and  an encoding attribute. The hash can be used as an indirect reference to the data.


## -parameters




### -param pSubjectInfo [in]

A pointer to a <a href="https://msdn.microsoft.com/6274cd08-d67f-410d-9303-3a42b7f1edc6">SIP_SUBJECTINFO</a> structure that contains the subject to which the indirect data reference will point.


### -param pcbIndirectData [in, out]

A pointer to a <b>DWORD</b> value to receive the size of the returned  <a href="https://msdn.microsoft.com/d34b599b-fe49-47c4-bb52-73ee14d73253">SIP_INDIRECT_DATA</a> structure.


### -param pIndirectData [out]

A pointer to a <a href="https://msdn.microsoft.com/d34b599b-fe49-47c4-bb52-73ee14d73253">SIP_INDIRECT_DATA</a> structure to receive the catalog item.


## -returns



The return value is <b>TRUE</b> if the function succeeds; otherwise, <b>FALSE</b>.


If this function returns <b>FALSE</b>, additional error information can be obtained by calling the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function. <b>GetLastError</b> will return one of the following error codes.



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
The file or data format is not correct for the specified <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">subject interface package</a> (SIP) type.

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



