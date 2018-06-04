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

# _CERT_USAGE_MATCH structure


## -description



			The <b>CERT_USAGE_MATCH</b> structure provides criteria for identifying issuer certificates to be used to build a certificate chain.


## -struct-fields




### -field dwType

Determines the kind of issuer matching to be done. In <b>AND</b> logic, the certificate must meet all criteria. In <b>OR</b> logic, the certificate must meet at least one of the criteria. The following codes are defined to determine the logic used in the match. For more information about how this applied, see Remarks.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="USAGE_MATCH_TYPE_AND"></a><a id="usage_match_type_and"></a><dl>
<dt><b>USAGE_MATCH_TYPE_AND</b></dt>
</dl>
</td>
<td width="60%">
<b>AND</b> logic

</td>
</tr>
<tr>
<td width="40%"><a id="USAGE_MATCH_TYPE_OR"></a><a id="usage_match_type_or"></a><dl>
<dt><b>USAGE_MATCH_TYPE_OR</b></dt>
</dl>
</td>
<td width="60%">
<b>OR</b> logic

</td>
</tr>
</table>
 

Default usage match logic is USAGE_MATCH_TYPE_AND.


### -field Usage


<a href="https://msdn.microsoft.com/70ee138a-df94-4fc4-9de5-0d8b7704b890">CERT_ENHKEY_USAGE</a> structure (<b>CERT_ENHKEY_USAGE</b> is an alternate typedef name for the <b>CTL_USAGE</b> structure) that includes an array of certificate <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifiers</a> (OIDs) that a certificate must match in order to be valid.


## -remarks



If the <i>dwType</i> member is set to <b>USAGE_MATCH_TYPE_OR</b>, the <i>Usage</i> member cannot be empty.

If the <i>dwType</i> member is set to <b>USAGE_MATCH_TYPE_AND</b>, an empty <i>Usage</i> member means that any nested usage in the chain will work.

The following describes the behavior given two enhanced key usage (EKU) extensions EKU A and EKU B.

<h3><a id="AND_Logic"></a><a id="and_logic"></a><a id="AND_LOGIC"></a>AND Logic</h3>
 If the caller specifies EKU A AND EKU B then the target certificate is valid if EKU A and EKU B are supported by every certificate in the path (either by an explicit EKU setting or through an absent EKU extension in CA certificates.)

<h3><a id="OR_Logic"></a><a id="or_logic"></a><a id="OR_LOGIC"></a>OR Logic</h3>
If the caller specifies EKU A OR EKU B then the target certificate is valid if either EKU A or EKU B is supported in the path.

 Besides the simple case where the certificates in the path contain EKU A or EKU B, the <b>OR</b> clause has the following special evaluation.

Given the following path, the <b>OR</b> test is deemed valid:

 Although the intersection of the EKUs in the chain is an empty set, the use of the EE certificate is valid for EKU A because the request to the cryptography API specifies that the certificate is valid if each certificate of the path supports either EKU A OR EKU B. 



