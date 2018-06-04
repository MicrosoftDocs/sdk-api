---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# PFNCMFILTERPROC callback function


## -description


The <b>PFNCMFILTERPROC</b> function is a filter procedure that filters each certificate to determine whether it will appear in the certificate selection dialog box that is displayed by the <a href="https://msdn.microsoft.com/8160ea08-c7c0-40f5-8771-6603f768744b">CertSelectCertificate</a> function.  <b>PFNCMFILTERPROC</b> is an application-defined callback function that is specified in the <a href="https://msdn.microsoft.com/49184872-d636-4e55-8e32-0f38b49b5c21">CERT_SELECT_STRUCT</a> structure. The <b>CERT_SELECT_STRUCT</b> structure is a parameter in the <a href="https://msdn.microsoft.com/8160ea08-c7c0-40f5-8771-6603f768744b">CertSelectCertificate</a> function. The <b>PFNCMFILTERPROC</b> function must be implemented by the developer to suit each application.


## -parameters




### -param pCertContext [in]

A pointer to a <a href="https://msdn.microsoft.com/f0a3200e-6541-423d-a4a3-595a31026eea">CERT_CONTEXT</a> structure that contains a certificate to make a filtering determination on.


### -param LPARAM


### -param DWORD








#### - dwDisplayWell [in]

 Reserved for future use.


#### - dwFlags [in]

 Reserved for future use.


#### - lCustData [in]

The address of an array of byte values that holds custom data.  <i>lCustData</i> is passed to the <b>PFNCMFILTERPROC</b> function by the <a href="https://msdn.microsoft.com/8160ea08-c7c0-40f5-8771-6603f768744b">CertSelectCertificate</a> function.


## -returns



Return a nonzero value (<b>TRUE</b>) to display the certificate. Return zero (<b>FALSE</b>) to not display the certificate.




## -see-also




<a href="https://msdn.microsoft.com/49184872-d636-4e55-8e32-0f38b49b5c21">CERT_SELECT_STRUCT</a>



<a href="https://msdn.microsoft.com/8160ea08-c7c0-40f5-8771-6603f768744b">CertSelectCertificate</a>
 

 

