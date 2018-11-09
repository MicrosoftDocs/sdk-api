---
UID: NF:mssip.CryptSIPRetrieveSubjectGuid
title: CryptSIPRetrieveSubjectGuid function
author: windows-sdk-content
description: Retrieves a GUID based on the header information in a specified file.
old-location: security\cryptsipretrievesubjectguid.htm
tech.root: seccrypto
ms.assetid: b81472bc-6d9c-4634-a378-e39786a0ca09
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: CryptSIPRetrieveSubjectGuid, CryptSIPRetrieveSubjectGuid function [Security], mssip/CryptSIPRetrieveSubjectGuid, security.cryptsipretrievesubjectguid
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
 - CryptSIPRetrieveSubjectGuid
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CryptSIPRetrieveSubjectGuid function


## -description


The <b>CryptSIPRetrieveSubjectGuid</b> function retrieves a GUID based on the header information in  a specified file. The GUID is used by the <a href="https://msdn.microsoft.com/3378ecee-bd5d-45e5-9a1f-a3734d086782">CryptSIPLoad</a> function to load the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">subject interface package</a> (SIP) implementation for the given file type.


## -parameters




### -param FileName [in]

The name of the file.


### -param hFileIn [in, optional]

A handle to the file to check. 


### -param pgSubject [out]

A GUID that identifies the subject.


## -returns



If the function succeeds, the function returns <b>TRUE</b>.

If the function fails, it returns  <b>FALSE</b>. For extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.



