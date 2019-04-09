---
UID: NN:certenroll.ICspInformation
title: ICspInformation (certenroll.h)
author: windows-sdk-content
description: Provides access to general information about a cryptographic provider.
old-location: security\icspinformation.htm
tech.root: seccertenroll
ms.assetid: e337ae2c-6f86-4025-8d31-47bc5d8a4ca8
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ICspInformation, ICspInformation interface [Security], ICspInformation interface [Security],described, certenroll/ICspInformation, security.icspinformation
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
 - ICspInformation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICspInformation interface


## -description


The <b>ICspInformation</b> interface provides access to general information about a cryptographic  provider. The information is initialized by calling the <a href="https://msdn.microsoft.com/b405503f-2af5-4a2f-abdb-e2eb108c4b1b">InitializeFromName</a> or <a href="https://msdn.microsoft.com/24466981-2ea2-41f5-b2db-85b5629fba7d">InitializeFromType</a> method. The information is retrieved by using the following methods and properties. For information about CSPs, see <a href="https://msdn.microsoft.com/7977e59b-7ce1-4bb4-aae4-d67b7d646493">CSPs and the Cryptography Process</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICspInformation</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>ICspInformation</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>ICspInformation</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6b551e72-2f0a-4ae8-ba06-dff1508a7d83">GetCspStatusFromOperations</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://msdn.microsoft.com/30cc43c8-6ef3-49ad-8cff-9a5b7389ff68">ICspStatus</a> object for the first supported algorithm that is consistent with the specified signature, encryption, hashing, or cipher  operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b4594400-29f2-47e2-8b4f-87ee82ea5e82">GetDefaultSecurityDescriptor</a>
</td>
<td align="left" width="63%">
Retrieves the default private key security descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b405503f-2af5-4a2f-abdb-e2eb108c4b1b">InitializeFromName</a>
</td>
<td align="left" width="63%">
Initializes the object from a string that contains a provider name.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/24466981-2ea2-41f5-b2db-85b5629fba7d">InitializeFromType</a>
</td>
<td align="left" width="63%">
Initializes the object from the default cryptographic provider.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICspInformation</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/e74f1aa3-883b-40e4-8052-6651eaa4b63f">CspAlgorithms</a>


</td>
<td align="left" width="63%">
Retrieves a collection of <a href="https://msdn.microsoft.com/08eba616-2e96-40cd-9fda-8549de98c138">ICspAlgorithm</a> interfaces that contain information about the algorithms supported by the provider.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/49d79310-90d2-4874-beaf-284abefd950f">HasHardwareRandomNumberGenerator</a>


</td>
<td align="left" width="63%">
Retrieves a Boolean value that specifies whether the provider supports a hardware random number generator that can be used to create random bytes for cryptographic operations.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/d69ade8c-3b74-4391-9048-6511f3d7e9fa">IsHardwareDevice</a>


</td>
<td align="left" width="63%">
Retrieves a Boolean value that determines whether the provider is implemented in a hardware device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/ee67670b-80a9-4637-a5ed-84d3430853ea">IsRemovable</a>


</td>
<td align="left" width="63%">
Retrieves a Boolean value that specifies whether the token that contains the key can be removed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/cfb88e17-39bb-4b4f-9eb3-3691376f8285">IsSmartCard</a>


</td>
<td align="left" width="63%">
Retrieves a Boolean value that specifies whether the provider is a smart card provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/50f78dcc-4d32-40c9-8153-f0b6ac72c03b">IsSoftwareDevice</a>


</td>
<td align="left" width="63%">
Retrieves a Boolean value that specifies whether the provider is implemented in software.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/f66f2f5c-7f50-4be6-973e-844d6cb76f61">KeySpec</a>


</td>
<td align="left" width="63%">
Retrieves a value that specifies the intended use of the algorithms supported by the provider.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/f798401c-bc78-438d-8847-82a57589ce38">LegacyCsp</a>


</td>
<td align="left" width="63%">
Retrieves a Boolean value that specifies whether the provider is a Cryptography API: Next Generation (CNG) provider or a CryptoAPI (legacy) CSP.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/2508786f-0892-4ece-bbef-bd8ed9c81eee">MaxKeyContainerNameLength</a>


</td>
<td align="left" width="63%">
Retrieves the maximum supported length for the name of the private key container associated with the provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/86f6993d-c96e-4753-9670-fdcc30e8c019">Name</a>


</td>
<td align="left" width="63%">
Retrieves the name of the provider.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/a52caea6-fbd5-4c06-8a25-e65f7b4a72f7">Type</a>


</td>
<td align="left" width="63%">
Retrieves the type of the provider.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/507896b0-598c-4a2d-854e-d4d266fdfaf7">Valid</a>


</td>
<td align="left" width="63%">
Retrieves a Boolean value that specifies whether the provider is installed on the client computer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/9b5010e3-d4c2-4194-ad8a-f8f4e0a41446">Version</a>


</td>
<td align="left" width="63%">
Retrieves the version number of the provider.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/d49511ed-8651-457e-a102-0bea4edde24c">CertEnroll Interfaces</a>



<a href="https://msdn.microsoft.com/8141023c-c162-46d6-9c37-e227ce1c8761">ICspInformations</a>



<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>
 

 

