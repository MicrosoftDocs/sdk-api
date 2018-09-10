---
UID: NF:cryptdlg.CertSelectCertificateW
title: CertSelectCertificateW function
author: windows-sdk-content
description: Presents a dialog box that allows the user to select certificates from a set of certificates that match the given criteria.
old-location: security\certselectcertificate.htm
tech.root: seccrypto
ms.assetid: 8160ea08-c7c0-40f5-8771-6603f768744b
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: CertSelectCertificate, CertSelectCertificate function [Security], CertSelectCertificateA, CertSelectCertificateW, cryptdlg/CertSelectCertificate, cryptdlg/CertSelectCertificateA, cryptdlg/CertSelectCertificateW, security.certselectcertificate
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: cryptdlg.h
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
 - CertSelectCertificate
 - CertSelectCertificateA
 - CertSelectCertificateW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CertSelectCertificateW function


## -description


The <b>CertSelectCertificate</b> function  presents a dialog box that allows the user to select certificates from a set of certificates that match the given criteria.
<div class="alert"><b>Note</b>  This function has no associated import library. You must use the <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> and <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> functions to dynamically link to CryptDlg.dll.</div><div> </div>

## -parameters




### -param pCertSelectInfo [in, out]

A pointer to a <a href="https://msdn.microsoft.com/en-us/library/Aa377534(v=VS.85).aspx">CERT_SELECT_STRUCT</a> structure that contains criteria that control the displayed certificates for selection and receives the selected certificate.


## -returns



If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. For extended error information, call the 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa377534(v=VS.85).aspx">CERT_SELECT_STRUCT</a>
 

 

