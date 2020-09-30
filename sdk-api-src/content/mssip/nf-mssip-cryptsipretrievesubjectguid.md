---
UID: NF:mssip.CryptSIPRetrieveSubjectGuid
title: CryptSIPRetrieveSubjectGuid function (mssip.h)
description: Retrieves a GUID based on the header information in a specified file.
helpviewer_keywords: ["CryptSIPRetrieveSubjectGuid","CryptSIPRetrieveSubjectGuid function [Security]","mssip/CryptSIPRetrieveSubjectGuid","security.cryptsipretrievesubjectguid"]
old-location: security\cryptsipretrievesubjectguid.htm
tech.root: security
ms.assetid: b81472bc-6d9c-4634-a378-e39786a0ca09
ms.date: 12/05/2018
ms.keywords: CryptSIPRetrieveSubjectGuid, CryptSIPRetrieveSubjectGuid function [Security], mssip/CryptSIPRetrieveSubjectGuid, security.cryptsipretrievesubjectguid
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
 - CryptSIPRetrieveSubjectGuid
 - mssip/CryptSIPRetrieveSubjectGuid
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
 - CryptSIPRetrieveSubjectGuid
---

# CryptSIPRetrieveSubjectGuid function


## -description

The <b>CryptSIPRetrieveSubjectGuid</b> function retrieves a GUID based on the header information in  a specified file. The GUID is used by the <a href="/windows/desktop/api/mssip/nf-mssip-cryptsipload">CryptSIPLoad</a> function to load the <a href="/windows/desktop/SecGloss/s-gly">subject interface package</a> (SIP) implementation for the given file type.

## -parameters

### -param FileName [in]

The name of the file.

### -param hFileIn [in, optional]

A handle to the file to check.

### -param pgSubject [out]

A GUID that identifies the subject.

## -returns

If the function succeeds, the function returns <b>TRUE</b>.

If the function fails, it returns  <b>FALSE</b>. For extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.