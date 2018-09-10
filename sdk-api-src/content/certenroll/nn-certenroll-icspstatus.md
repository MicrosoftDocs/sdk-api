---
UID: NN:certenroll.ICspStatus
title: ICspStatus
author: windows-sdk-content
description: Contains information about a cryptographic provider/algorithm pair.
old-location: security\icspstatus.htm
tech.root: SecCertEnroll
ms.assetid: 30cc43c8-6ef3-49ad-8cff-9a5b7389ff68
ms.author: windowssdkdev
ms.date: 08/29/2018
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


An <b>ICspStatus</b> object contains information about a  cryptographic provider/algorithm pair. The object is primarily used by the Certificate Enrollment Control to enable a user to select which cryptographic providers and algorithms to use when creating a certificate request. It can be retrieved, either alone or in an  <a href="https://msdn.microsoft.com/73d0f3a7-7afd-42c9-88db-911531c50137">ICspStatuses</a> collection, by calling the following properties or methods:<table>
<tr>
<th>Property/Method</th>
<th>Interface</th>
<th>Description</th>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/6b551e72-2f0a-4ae8-ba06-dff1508a7d83">GetCspStatusFromOperations</a>
</td>
<td>
<a href="https://msdn.microsoft.com/e337ae2c-6f86-4025-8d31-47bc5d8a4ca8">ICspInformation</a>
</td>
<td>Creates an <b>ICspStatus</b> object for the first supported algorithm that is consistent with a specified algorithm object identifier (OID) and algorithm type.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/7c099357-8299-4664-ba16-7f8936e16054">GetCspStatusesFromOperations</a>
</td>
<td>
<a href="https://msdn.microsoft.com/8141023c-c162-46d6-9c37-e227ce1c8761">ICspInformations</a>
</td>
<td>Creates an <a href="https://msdn.microsoft.com/73d0f3a7-7afd-42c9-88db-911531c50137">ICspStatuses</a> collection for a specified algorithm type and optional provider information.<div class="alert"><b>Note</b>  The Certificate Enrollment Control uses an <a href="https://msdn.microsoft.com/73d0f3a7-7afd-42c9-88db-911531c50137">ICspStatuses</a> collection only for private key asymmetric (encryption, signing, and key exchange) algorithm  selection.</div>
<div> </div>
</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/f73d40cb-dde3-46a5-ba9f-f7cbfa2efe70">GetCspStatusFromProviderName</a>
</td>
<td>
<a href="https://msdn.microsoft.com/8141023c-c162-46d6-9c37-e227ce1c8761">ICspInformations</a>
</td>
<td>Creates an <b>ICspStatus</b> object for a legacy provider by provider name and supported key operations.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/8bf6e62d-9ecf-4eee-9652-f04d2010b4f7">CspStatus</a>
</td>
<td>
<a href="https://msdn.microsoft.com/72612ea4-ed45-46ac-9dad-614a9a754d83">IX509PrivateKey</a>
</td>
<td>Specifies or retrieves an <b>ICspStatus</b> object. The  object is typically created during the enrollment process.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/50dc8cc5-21ee-4347-a12a-0d6e62901fbb">GetCspStatuses</a>
</td>
<td>
<a href="https://msdn.microsoft.com/5b3764dc-fc63-45cc-8c35-65539c461e81">IX509CertificateRequestPkcs10</a>
</td>
<td>Creates an <a href="https://msdn.microsoft.com/73d0f3a7-7afd-42c9-88db-911531c50137">ICspStatuses</a> collection that contains all  provider/algorithm pairs consistent with the intended use of the private key as specified by the caller.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/cad6d8f0-f7d6-4ede-96a2-b00159962a1b">CspStatuses</a>
</td>
<td>
<a href="https://msdn.microsoft.com/5b3764dc-fc63-45cc-8c35-65539c461e81">IX509CertificateRequestPkcs10</a>
</td>
<td>Creates an <a href="https://msdn.microsoft.com/73d0f3a7-7afd-42c9-88db-911531c50137">ICspStatuses</a> collection that contains all  provider/algorithm pairs consistent with the intended use of the private key as identified by the <a href="https://msdn.microsoft.com/72612ea4-ed45-46ac-9dad-614a9a754d83">IX509PrivateKey</a> object associated with the certificate request.</td>
</tr>
</table>
 



Because cryptographic providers typically support more than one algorithm, multiple <b>ICspStatus</b> objects may be created and returned when you call any of the preceding properties or methods that return a collection. This is shown by the following  illustration:

<img alt="Structure of the ICspStatuses collection showing individual ICspStatus objects" src="./images/ICSPStatuses.png"/>

You can use the <a href="https://msdn.microsoft.com/56798477-ec12-47b6-a226-d20258677033">EnrollmentStatus</a> property on an <b>ICspStatus</b> object to retrieve an <a href="https://msdn.microsoft.com/fa5e3a10-7f00-46b6-b740-b72d78745bf7">IX509EnrollmentStatus</a> object that defines the following properties:<ul>
<li>The <a href="https://msdn.microsoft.com/91ac74af-8e59-42fc-bca8-d7ef96a1fed0">Display</a> property specifies whether the provider/algorithm pair can be displayed in a user interface.</li>
<li>The <a href="https://msdn.microsoft.com/9050f394-ccad-4a6e-90bc-53af3a874f91">Selected</a> property specifies or retrieves a value that indicates whether the status of a specific item is monitored during the enrollment process.</li>
<li>The <a href="https://msdn.microsoft.com/ca1105eb-a29a-458d-abbb-34c9b67d7c8a">Status</a> property identifies the status of the enrollment process.</li>
</ul>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICspStatus</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>ICspStatus</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
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
<a href="https://msdn.microsoft.com/dc5f92e8-29fe-474c-bf1d-c6d7716abce1">Initialize</a>
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

<a href="https://msdn.microsoft.com/fc86ff4a-98f4-4e14-8d24-132926c9b41d">CspAlgorithm</a>


</td>
<td align="left" width="63%">
Retrieves an <a href="https://msdn.microsoft.com/08eba616-2e96-40cd-9fda-8549de98c138">ICspAlgorithm</a> object that contains information about an algorithm supported by the provider.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/9e9202ad-086e-493b-8830-0a0f8980cec5">CspInformation</a>


</td>
<td align="left" width="63%">
Retrieves an <a href="https://msdn.microsoft.com/e337ae2c-6f86-4025-8d31-47bc5d8a4ca8">ICspInformation</a> object that contains general information about the provider.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/7c778f78-1e94-4e84-a51a-3c0171f19db6">DisplayName</a>


</td>
<td align="left" width="63%">
Retrieves a string that contains the name of the provider, the algorithm name, and the operations that can be performed by the algorithm.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/56798477-ec12-47b6-a226-d20258677033">EnrollmentStatus</a>


</td>
<td align="left" width="63%">
Retrieves an <a href="https://msdn.microsoft.com/fa5e3a10-7f00-46b6-b740-b72d78745bf7">IX509EnrollmentStatus</a> object that contains information about the certificate enrollment.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/e392e28f-084e-43a7-8a5e-14bea0ed8d58">Ordinal</a>


</td>
<td align="left" width="63%">
Specifies or retrieves the  position of the <b>ICspStatus</b> object in the <a href="https://msdn.microsoft.com/73d0f3a7-7afd-42c9-88db-911531c50137">ICspStatuses</a> collection.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/d49511ed-8651-457e-a102-0bea4edde24c">CertEnroll Interfaces</a>



<a href="https://msdn.microsoft.com/73d0f3a7-7afd-42c9-88db-911531c50137">ICspStatuses</a>



<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>
 

 

