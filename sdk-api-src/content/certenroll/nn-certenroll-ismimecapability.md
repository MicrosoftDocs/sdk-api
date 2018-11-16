---
UID: NN:certenroll.ISmimeCapability
title: ISmimeCapability
author: windows-sdk-content
description: Represents an SMIMECapabilities extension that identifies the decryption capabilities of an email recipient.
old-location: security\ismimecapability.htm
tech.root: SecCertEnroll
ms.assetid: 3cfbb16f-88fa-41f1-b719-cd5e8ad636cc
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ISmimeCapability, ISmimeCapability interface [Security], ISmimeCapability interface [Security],described, certenroll/ISmimeCapability, security.ismimecapability
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
 - ISmimeCapability
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISmimeCapability interface


## -description


A collection of <b>ISmimeCapability</b> objects represents an <b>SMIMECapabilities</b> extension that identifies the  decryption capabilities of an email recipient. The extension includes a collection of <b>ISmimeCapability</b> objects, each of which identifies a symmetric encryption algorithm supported by the client, and an optional bit length that indicates the relative strength of the algorithm. The following syntax shows the <a href="https://msdn.microsoft.com/en-us/library/ms721532(v=VS.85).aspx">Abstract Syntax Notation One</a> (ASN.1) structure  of the extension. The extension is represented by an <a href="https://msdn.microsoft.com/en-us/library/Aa378177(v=VS.85).aspx">IX509ExtensionSmimeCapabilities</a> interface.
<pre class="syntax" xml:space="preserve"><code>
----------------------------------------------------------------------
-- SMIMECapabilities
-- XCN_OID_RSA_SMIMECapabilities (1.2.840.113549.1.9.15)
----------------------------------------------------------------------

SMIMECapabilities ::= SEQUENCE OF SMIMECapability

SMIMECapability ::= SEQUENCE 
{
   capabilityID    EncodedObjectID,
   smimeParameters ANY OPTIONAL    
}
</code></pre>The extension is used to report the decryption capabilities of an email recipient to an email sender. This enables the sender to choose the most secure algorithm supported by both parties.

The optional bit length is used to identify the length of the encryption key used by algorithm. The key length is implicitly defined by the object identifier for the AES, DES, and 3DES algorithms, but it is variable for the RC2 and RC4 algorithms. If you specify a key length, it must be consistent with that supported by the cryptographic  providers used by the client. For more information, see <a href="https://msdn.microsoft.com/en-us/library/Aa375967(v=VS.85).aspx">ICspInformation</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISmimeCapability</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>ISmimeCapability</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Properties</a></li>
</ul>

## -members

The <b>ISmimeCapability</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa377047(v=VS.85).aspx">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the object from a symmetric encryption algorithm object identifier and an optional key length.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISmimeCapability</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa377046(v=VS.85).aspx">BitCount</a>


</td>
<td align="left" width="63%">
Retrieves the length, in bits, of the encryption key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa377049(v=VS.85).aspx">ObjectId</a>


</td>
<td align="left" width="63%">
Retrieves the object identifier of the symmetric encryption algorithm.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa374874(v=VS.85).aspx">Certificate Enrollment API</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa375947(v=VS.85).aspx">ICspAlgorithm</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa375967(v=VS.85).aspx">ICspInformation</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa376841(v=VS.85).aspx">ISmimeCapabilities</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa378177(v=VS.85).aspx">IX509ExtensionSmimeCapabilities</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa378174(v=VS.85).aspx">IX509Extensions</a>
 

 

