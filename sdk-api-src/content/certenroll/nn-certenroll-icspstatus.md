---
UID: NN:certenroll.ICspStatus
title: ICspStatus
author: windows-sdk-content
description: Contains information about a cryptographic provider/algorithm pair.
old-location: security\icspstatus.htm
tech.root: seccertenroll
ms.assetid: 30cc43c8-6ef3-49ad-8cff-9a5b7389ff68
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: ICspStatus, ICspStatus interface [Security], ICspStatus interface [Security],described, certenroll/ICspStatus, security.icspstatus
ms.prod: windows
ms.technology: windows-sdk
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
 - ICspStatus
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICspStatus interface


## -description


An <b>ICspStatus</b> object contains information about a  cryptographic provider/algorithm pair. The object is primarily used by the Certificate Enrollment Control to enable a user to select which cryptographic providers and algorithms to use when creating a certificate request. It can be retrieved, either alone or in an  <a href="https://msdn.microsoft.com/en-us/library/Aa376761(v=VS.85).aspx">ICspStatuses</a> collection, by calling the following properties or methods:<table>
<tr>
<th>Property/Method</th>
<th>Interface</th>
<th>Description</th>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Aa376624(v=VS.85).aspx">GetCspStatusFromOperations</a>
</td>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Aa375967(v=VS.85).aspx">ICspInformation</a>
</td>
<td>Creates an <b>ICspStatus</b> object for the first supported algorithm that is consistent with a specified algorithm object identifier (OID) and algorithm type.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Aa965589(v=VS.85).aspx">GetCspStatusesFromOperations</a>
</td>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Aa375968(v=VS.85).aspx">ICspInformations</a>
</td>
<td>Creates an <a href="https://msdn.microsoft.com/en-us/library/Aa376761(v=VS.85).aspx">ICspStatuses</a> collection for a specified algorithm type and optional provider information.<div class="alert"><b>Note</b>  The Certificate Enrollment Control uses an <a href="https://msdn.microsoft.com/en-us/library/Aa376761(v=VS.85).aspx">ICspStatuses</a> collection only for private key asymmetric (encryption, signing, and key exchange) algorithm  selection.</div>
<div> </div>
</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Aa965590(v=VS.85).aspx">GetCspStatusFromProviderName</a>
</td>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Aa375968(v=VS.85).aspx">ICspInformations</a>
</td>
<td>Creates an <b>ICspStatus</b> object for a legacy provider by provider name and supported key operations.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Aa378972(v=VS.85).aspx">CspStatus</a>
</td>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Aa378921(v=VS.85).aspx">IX509PrivateKey</a>
</td>
<td>Specifies or retrieves an <b>ICspStatus</b> object. The  object is typically created during the enrollment process.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Aa965815(v=VS.85).aspx">GetCspStatuses</a>
</td>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Aa377505(v=VS.85).aspx">IX509CertificateRequestPkcs10</a>
</td>
<td>Creates an <a href="https://msdn.microsoft.com/en-us/library/Aa376761(v=VS.85).aspx">ICspStatuses</a> collection that contains all  provider/algorithm pairs consistent with the intended use of the private key as specified by the caller.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Aa377517(v=VS.85).aspx">CspStatuses</a>
</td>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Aa377505(v=VS.85).aspx">IX509CertificateRequestPkcs10</a>
</td>
<td>Creates an <a href="https://msdn.microsoft.com/en-us/library/Aa376761(v=VS.85).aspx">ICspStatuses</a> collection that contains all  provider/algorithm pairs consistent with the intended use of the private key as identified by the <a href="https://msdn.microsoft.com/en-us/library/Aa378921(v=VS.85).aspx">IX509PrivateKey</a> object associated with the certificate request.</td>
</tr>
</table>
 



Because cryptographic providers typically support more than one algorithm, multiple <b>ICspStatus</b> objects may be created and returned when you call any of the preceding properties or methods that return a collection. This is shown by the following  illustration:

<img alt="Structure of the ICspStatuses collection showing individual ICspStatus objects" src="images/ICSPStatuses.png"/>

You can use the <a href="https://msdn.microsoft.com/en-us/library/Aa376775(v=VS.85).aspx">EnrollmentStatus</a> property on an <b>ICspStatus</b> object to retrieve an <a href="https://msdn.microsoft.com/en-us/library/Aa377818(v=VS.85).aspx">IX509EnrollmentStatus</a> object that defines the following properties:<ul>
<li>The <a href="https://msdn.microsoft.com/en-us/library/Aa377826(v=VS.85).aspx">Display</a> property specifies whether the provider/algorithm pair can be displayed in a user interface.</li>
<li>The <a href="https://msdn.microsoft.com/en-us/library/Aa377841(v=VS.85).aspx">Selected</a> property specifies or retrieves a value that indicates whether the status of a specific item is monitored during the enrollment process.</li>
<li>The <a href="https://msdn.microsoft.com/en-us/library/Aa377844(v=VS.85).aspx">Status</a> property identifies the status of the enrollment process.</li>
</ul>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICspStatus</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>ICspStatus</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Properties</a></li>
</ul>

## -members

The <b>ICspStatus</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa376776(v=VS.85).aspx">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the object from a cryptographic provider and an associated algorithm.

[WebEnabled]

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICspStatus</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa376772(v=VS.85).aspx">CspAlgorithm</a>


</td>
<td align="left" width="63%">
Retrieves an <a href="https://msdn.microsoft.com/en-us/library/Aa375947(v=VS.85).aspx">ICspAlgorithm</a> object that contains information about an algorithm supported by the provider.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa376773(v=VS.85).aspx">CspInformation</a>


</td>
<td align="left" width="63%">
Retrieves an <a href="https://msdn.microsoft.com/en-us/library/Aa375967(v=VS.85).aspx">ICspInformation</a> object that contains general information about the provider.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa376774(v=VS.85).aspx">DisplayName</a>


</td>
<td align="left" width="63%">
Retrieves a string that contains the name of the provider, the algorithm name, and the operations that can be performed by the algorithm.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa376775(v=VS.85).aspx">EnrollmentStatus</a>


</td>
<td align="left" width="63%">
Retrieves an <a href="https://msdn.microsoft.com/en-us/library/Aa377818(v=VS.85).aspx">IX509EnrollmentStatus</a> object that contains information about the certificate enrollment.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa376779(v=VS.85).aspx">Ordinal</a>


</td>
<td align="left" width="63%">
Specifies or retrieves the  position of the <b>ICspStatus</b> object in the <a href="https://msdn.microsoft.com/en-us/library/Aa376761(v=VS.85).aspx">ICspStatuses</a> collection.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa374850(v=VS.85).aspx">CertEnroll Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa376761(v=VS.85).aspx">ICspStatuses</a>



<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>
 

 

