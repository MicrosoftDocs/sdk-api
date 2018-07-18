---
UID: NF:cryptdlg.GetFriendlyNameOfCertA
title: GetFriendlyNameOfCertA function
author: windows-sdk-content
description: Retrieves the display name for a certificate.
old-location: security\getfriendlynameofcert.htm
old-project: seccrypto
ms.assetid: a66a8573-b234-4d5d-bd38-72a3a44a0419
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: GetFriendlyNameOfCert, GetFriendlyNameOfCert function [Security], GetFriendlyNameOfCertA, GetFriendlyNameOfCertW, cryptdlg/GetFriendlyNameOfCert, cryptdlg/GetFriendlyNameOfCertA, cryptdlg/GetFriendlyNameOfCertW, security.getfriendlynameofcert
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: cryptdlg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetFriendlyNameOfCertW (Unicode) and GetFriendlyNameOfCertA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: SecPkgContext_ClientCreds, *PSecPkgContext_ClientCreds
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - CryptDlg.dll
api_name:
 - GetFriendlyNameOfCert
 - GetFriendlyNameOfCertA
 - GetFriendlyNameOfCertW
product: Windows
targetos: Windows
req.lib: 
req.dll: CryptDlg.dll
req.irql: 
---

# GetFriendlyNameOfCertA function


## -description


<p class="CCE_Message">[The <b>GetFriendlyNameOfCert</b> function is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/300e6345-0be0-48c7-a3a3-174879cf0bbb">CertGetNameString</a> function with the CERT_NAME_FRIENDLY_DISPLAY_TYPE flag.]

The <b>GetFriendlyNameOfCert</b> function retrieves the display name for a certificate.
<div class="alert"><b>Note</b>  This function has no associated import library. You must use the <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> and <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> functions to dynamically link to CryptDlg.dll.</div><div> </div>

## -parameters




### -param pccert [in]

A pointer to the certificate context whose display name is being retrieved.


### -param pch

TBD


### -param cch

TBD




#### - cchBuffer [in]

Number of characters allocated for <i>pchBuffer</i>, including the terminating <b>NULL</b> character.


#### - pchBuffer [out]

A pointer to a character string that receives the display name for the certificate.


## -returns



The return value is the number of characters, including the terminating <b>NULL</b> character, in the returned display name.



