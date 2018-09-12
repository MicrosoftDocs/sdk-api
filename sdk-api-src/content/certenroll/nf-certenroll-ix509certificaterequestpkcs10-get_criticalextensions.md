---
UID: NF:certenroll.IX509CertificateRequestPkcs10.get_CriticalExtensions
title: IX509CertificateRequestPkcs10::get_CriticalExtensions
author: windows-sdk-content
description: Retrieves an IObjectIds collection that identifies the version 3 certificate extensions marked as critical.
old-location: security\ix509certificaterequestpkcs10_criticalextensions_property.htm
tech.root: SecCertEnroll
ms.assetid: 7ecde7cb-1a73-4fee-a949-c4bb36e61547
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: CriticalExtensions property [Security], CriticalExtensions property [Security],IX509CertificateRequestPkcs10 interface, IX509CertificateRequestPkcs10 interface [Security],CriticalExtensions property, IX509CertificateRequestPkcs10.CriticalExtensions, IX509CertificateRequestPkcs10.get_CriticalExtensions, IX509CertificateRequestPkcs10::CriticalExtensions, IX509CertificateRequestPkcs10::get_CriticalExtensions, certenroll/IX509CertificateRequestPkcs10::CriticalExtensions, certenroll/IX509CertificateRequestPkcs10::get_CriticalExtensions, get_CriticalExtensions, security.ix509certificaterequestpkcs10_criticalextensions_property
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: certenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.dll: CertEnroll.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - IX509CertificateRequestPkcs10.CriticalExtensions
 - IX509CertificateRequestPkcs10.get_CriticalExtensions
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509CertificateRequestPkcs10::get_CriticalExtensions


## -description


The <b>CriticalExtensions</b> property retrieves an <a href="https://msdn.microsoft.com/en-us/library/Aa376785(v=VS.85).aspx">IObjectIds</a> collection that identifies the version 3 certificate extensions marked as critical.

This property is read-only.


## -parameters


## -remarks



The extension criticality indicates to an application that uses certificates whether it can ignore the extension. You must initialize the <a href="https://msdn.microsoft.com/en-us/library/Aa377505(v=VS.85).aspx">IX509CertificateRequestPkcs10</a> object before calling this property. For more information, see any of the following methods:

<ul>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377520(v=VS.85).aspx">InitializeDecode</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377523(v=VS.85).aspx">InitializeFromCertificate</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377527(v=VS.85).aspx">InitializeFromPrivateKey</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377531(v=VS.85).aspx">InitializeFromPublicKey</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377533(v=VS.85).aspx">InitializeFromTemplateName</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa377505(v=VS.85).aspx">IX509CertificateRequestPkcs10</a>
 

 

