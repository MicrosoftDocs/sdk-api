---
UID: NF:cryptdlg.CertViewPropertiesA
title: CertViewPropertiesA function (cryptdlg.h)
author: windows-sdk-content
description: The CertViewProperties function displays the properties for a certificate in a user interface (UI) dialog box. This function has no associated import library. You must use the LoadLibrary and GetProcAddress functions to dynamically link to CryptDlg.dll.
old-location: security\certviewproperties.htm
tech.root: SecCrypto
ms.assetid: 5df840ab-fff6-4c7e-b799-51e4de4c644a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CertViewProperties, CertViewProperties function [Security], CertViewPropertiesA, CertViewPropertiesW, cryptdlg/CertViewProperties, cryptdlg/CertViewPropertiesA, cryptdlg/CertViewPropertiesW, security.certviewproperties
ms.topic: function
req.header: cryptdlg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CertViewPropertiesW (Unicode) and CertViewPropertiesA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: CryptDlg.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - CryptDlg.dll
api_name:
 - CertViewProperties
 - CertViewPropertiesA
 - CertViewPropertiesW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CertViewPropertiesA function


## -description


<p class="CCE_Message">[The <b>CertViewProperties</b> function is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/d4b8f01b-7c3e-4286-bc37-d5ec4a1e1c2f">CryptUIDlgViewContext</a> function.]

The <b>CertViewProperties</b> function displays the properties for a certificate in a user interface (UI) dialog box. This function has no associated import library. You must use the <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> and <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> functions to dynamically link to CryptDlg.dll.
<div class="alert"><b>Note</b>  This function has no associated import library. You must use the <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> and <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> functions to dynamically link to CryptDlg.dll.</div><div> </div>

## -parameters




### -param pCertViewInfo [in]

A pointer to a <a href="https://msdn.microsoft.com/3d18526b-1052-4f0c-999b-881a74a94549">CERT_VIEWPROPERTIES_STRUCT</a> structure that contains the information about the certificate to view.


## -returns



The return value is <b>TRUE</b> if the function is successful; <b>FALSE</b> if the function fails.



