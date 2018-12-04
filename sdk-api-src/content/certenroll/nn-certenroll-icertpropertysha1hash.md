---
UID: NN:certenroll.ICertPropertySHA1Hash
title: ICertPropertySHA1Hash
author: windows-sdk-content
description: Represents a certificate property that contains a SHA-1 hash of the certificate.
old-location: security\icertpropertysha1hash.htm
tech.root: seccertenroll
ms.assetid: 0946827b-c933-472c-9466-aaa3495ab202
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: ICertPropertySHA1Hash, ICertPropertySHA1Hash interface [Security], ICertPropertySHA1Hash interface [Security],described, certenroll/ICertPropertySHA1Hash, security.icertpropertysha1hash
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
 - ICertPropertySHA1Hash
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertPropertySHA1Hash interface


## -description


The <b>ICertPropertySHA1Hash</b> interface represents a certificate property that contains a SHA-1 hash of the certificate.  The hash functions as a unique identifier. Typically, it is called a thumb print.<div class="alert"><b>Note</b>  The <a href="https://msdn.microsoft.com/e7ad0ec5-a568-4506-ba54-908e00083c2b">CERTENROLL_PROPERTYID</a> value is XCN_CERT_SHA1_HASH_PROP_ID.</div>
<div> </div>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICertPropertySHA1Hash</b> interface inherits from <a href="https://msdn.microsoft.com/947c2f09-993d-4ced-8b76-66b79d96e3bc">ICertProperty</a>. <b>ICertPropertySHA1Hash</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>ICertPropertySHA1Hash</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/898da01b-94e6-4a07-9c53-f93378fbda8c">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the object from the SHA-1 hash of a certificate.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICertPropertySHA1Hash</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/28c6efb3-1cf7-4f3b-ad42-6f5d72d3117b">SHA1Hash</a>


</td>
<td align="left" width="63%">
Retrieves the SHA-1 hash of a certificate.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/d49511ed-8651-457e-a102-0bea4edde24c">CertEnroll Interfaces</a>



<a href="https://msdn.microsoft.com/947c2f09-993d-4ced-8b76-66b79d96e3bc">ICertProperty</a>
 

 

