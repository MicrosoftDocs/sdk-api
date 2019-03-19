---
UID: NF:mssip.CryptSIPVerifyIndirectData
title: CryptSIPVerifyIndirectData function (mssip.h)
author: windows-sdk-content
description: Validates the indirect hashed data against the supplied subject.
old-location: security\cryptsipverifyindirectdata.htm
tech.root: SecCrypto
ms.assetid: 137b8858-a31f-4ef6-96bd-c5e26ae7b3e8
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CryptSIPVerifyIndirectData, CryptSIPVerifyIndirectData function [Security], mssip/CryptSIPVerifyIndirectData, security.cryptsipverifyindirectdata
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
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Crypt32.dll
api_name:
 - CryptSIPVerifyIndirectData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CryptSIPVerifyIndirectData function


## -description


The <b>CryptSIPVerifyIndirectData</b> function validates the indirect hashed data against the supplied subject.


## -parameters




### -param pSubjectInfo [in]

A pointer to a <a href="https://msdn.microsoft.com/6274cd08-d67f-410d-9303-3a42b7f1edc6">SIP_SUBJECTINFO</a> structure that contains information about the message subject.


### -param pIndirectData [in]

A pointer to a <a href="https://msdn.microsoft.com/d34b599b-fe49-47c4-bb52-73ee14d73253">SIP_INDIRECT_DATA</a> structure that contains information about the hashed subject information.


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
<dt><b>TRUST_E_SUBJECT_FORM_UNKNOWN</b></dt>
</dl>
</td>
<td width="60%">
The subject type is an unknown type.

</td>
</tr>
</table>
 




## -remarks



Subjects include, but are not limited to, portable executable images (.exe), cabinet (.cab) images, flat files, and catalog files. Each subject type uses a different subset of its data for hash calculation and requires a different procedure for storage and retrieval. Therefore each subject type has a unique subject interface package specification.



