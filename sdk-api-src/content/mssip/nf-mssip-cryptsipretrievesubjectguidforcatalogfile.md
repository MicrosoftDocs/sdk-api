---
UID: NF:mssip.CryptSIPRetrieveSubjectGuidForCatalogFile
title: CryptSIPRetrieveSubjectGuidForCatalogFile function
author: windows-driver-content
description: Retrieves the subject GUID associated with the specified file.
old-location: security\cryptsipretrievesubjectguidforcatalogfile.htm
old-project: SecCrypto
ms.assetid: 7f757dc8-948c-476e-aca3-a9051e962ed4
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: CryptSIPRetrieveSubjectGuidForCatalogFile, CryptSIPRetrieveSubjectGuidForCatalogFile function [Security], mssip/CryptSIPRetrieveSubjectGuidForCatalogFile, security.cryptsipretrievesubjectguidforcatalogfile
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: SimilarityFileId
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Crypt32.dll
api_name:
-	CryptSIPRetrieveSubjectGuidForCatalogFile
product: Windows
targetos: Windows
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
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
</table>
 




## -remarks



This function only supports <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">subject interface packages</a> (SIPs) that are used for portable executable images (.exe), cabinet (.cab) images, and flat files.



