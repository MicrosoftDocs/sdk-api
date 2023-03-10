---
UID: NF:mssip.CryptSIPRetrieveSubjectGuidForCatalogFile
title: CryptSIPRetrieveSubjectGuidForCatalogFile function (mssip.h)
description: Retrieves the subject GUID associated with the specified file.
helpviewer_keywords: ["CryptSIPRetrieveSubjectGuidForCatalogFile","CryptSIPRetrieveSubjectGuidForCatalogFile function [Security]","mssip/CryptSIPRetrieveSubjectGuidForCatalogFile","security.cryptsipretrievesubjectguidforcatalogfile"]
old-location: security\cryptsipretrievesubjectguidforcatalogfile.htm
tech.root: security
ms.assetid: 7f757dc8-948c-476e-aca3-a9051e962ed4
ms.date: 12/05/2018
ms.keywords: CryptSIPRetrieveSubjectGuidForCatalogFile, CryptSIPRetrieveSubjectGuidForCatalogFile function [Security], mssip/CryptSIPRetrieveSubjectGuidForCatalogFile, security.cryptsipretrievesubjectguidforcatalogfile
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
 - CryptSIPRetrieveSubjectGuidForCatalogFile
 - mssip/CryptSIPRetrieveSubjectGuidForCatalogFile
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
 - CryptSIPRetrieveSubjectGuidForCatalogFile
---

# CryptSIPRetrieveSubjectGuidForCatalogFile function


## -description

The  <b>CryptSIPRetrieveSubjectGuidForCatalogFile</b> function retrieves the subject GUID associated with the specified file.

## -parameters

### -param FileName [in]

The name of the file. If the <i>hFileIn</i> parameter is set, the value in this parameter is ignored.

### -param hFileIn [in, optional]

A handle to the file to check. This parameter must contain a valid handle if the <i>FileName</i> parameter is <b>NULL</b>.

### -param pgSubject [out]

A globally unique ID that identifies the subject.

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
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One or more of the parameters are not valid.

</td>
</tr>
</table>

## -remarks

This function only supports <a href="/windows/desktop/SecGloss/s-gly">subject interface packages</a> (SIPs) that are used for portable executable images (.exe), cabinet (.cab) images, and flat files.