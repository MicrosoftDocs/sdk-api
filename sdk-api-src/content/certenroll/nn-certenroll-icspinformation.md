---
UID: NN:certenroll.ICspInformation
title: ICspInformation
author: windows-sdk-content
description: Provides access to general information about a cryptographic provider.
old-location: security\icspinformation.htm
tech.root: seccertenroll
ms.assetid: e337ae2c-6f86-4025-8d31-47bc5d8a4ca8
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: ICspInformation, ICspInformation interface [Security], ICspInformation interface [Security],described, certenroll/ICspInformation, security.icspinformation
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
 - ICspInformation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICspInformation interface


## -description


The <b>ICspInformation</b> interface provides access to general information about a cryptographic  provider. The information is initialized by calling the <a href="https://msdn.microsoft.com/en-us/library/Aa376745(v=VS.85).aspx">InitializeFromName</a> or <a href="https://msdn.microsoft.com/en-us/library/Aa376746(v=VS.85).aspx">InitializeFromType</a> method. The information is retrieved by using the following methods and properties. For information about CSPs, see <a href="https://msdn.microsoft.com/en-us/library/Aa381481(v=VS.85).aspx">CSPs and the Cryptography Process</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICspInformation</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>ICspInformation</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Properties</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/Aa376624(v=VS.85).aspx">GetCspStatusFromOperations</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://msdn.microsoft.com/en-us/library/Aa376760(v=VS.85).aspx">ICspStatus</a> object for the first supported algorithm that is consistent with the specified signature, encryption, hashing, or cipher  operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa376741(v=VS.85).aspx">GetDefaultSecurityDescriptor</a>
</td>
<td align="left" width="63%">
Retrieves the default private key security descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa376745(v=VS.85).aspx">InitializeFromName</a>
</td>
<td align="left" width="63%">
Initializes the object from a string that contains a provider name.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa376746(v=VS.85).aspx">InitializeFromType</a>
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

<a href="https://msdn.microsoft.com/en-us/library/Aa376605(v=VS.85).aspx">CspAlgorithms</a>


</td>
<td align="left" width="63%">
Retrieves a collection of <a href="https://msdn.microsoft.com/en-us/library/Aa375947(v=VS.85).aspx">ICspAlgorithm</a> interfaces that contain information about the algorithms supported by the provider.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa376743(v=VS.85).aspx">HasHardwareRandomNumberGenerator</a>


</td>
<td align="left" width="63%">
Retrieves a Boolean value that specifies whether the provider supports a hardware random number generator that can be used to create random bytes for cryptographic operations.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa376747(v=VS.85).aspx">IsHardwareDevice</a>


</td>
<td align="left" width="63%">
Retrieves a Boolean value that determines whether the provider is implemented in a hardware device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa376748(v=VS.85).aspx">IsRemovable</a>


</td>
<td align="left" width="63%">
Retrieves a Boolean value that specifies whether the token that contains the key can be removed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Bb394685(v=VS.85).aspx">IsSmartCard</a>


</td>
<td align="left" width="63%">
Retrieves a Boolean value that specifies whether the provider is a smart card provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa376750(v=VS.85).aspx">IsSoftwareDevice</a>


</td>
<td align="left" width="63%">
Retrieves a Boolean value that specifies whether the provider is implemented in software.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa376751(v=VS.85).aspx">KeySpec</a>


</td>
<td align="left" width="63%">
Retrieves a value that specifies the intended use of the algorithms supported by the provider.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa376752(v=VS.85).aspx">LegacyCsp</a>


</td>
<td align="left" width="63%">
Retrieves a Boolean value that specifies whether the provider is a Cryptography API: Next Generation (CNG) provider or a CryptoAPI (legacy) CSP.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa376753(v=VS.85).aspx">MaxKeyContainerNameLength</a>


</td>
<td align="left" width="63%">
Retrieves the maximum supported length for the name of the private key container associated with the provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa376755(v=VS.85).aspx">Name</a>


</td>
<td align="left" width="63%">
Retrieves the name of the provider.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa376757(v=VS.85).aspx">Type</a>


</td>
<td align="left" width="63%">
Retrieves the type of the provider.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa376758(v=VS.85).aspx">Valid</a>


</td>
<td align="left" width="63%">
Retrieves a Boolean value that specifies whether the provider is installed on the client computer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa376759(v=VS.85).aspx">Version</a>


</td>
<td align="left" width="63%">
Retrieves the version number of the provider.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa374850(v=VS.85).aspx">CertEnroll Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa375968(v=VS.85).aspx">ICspInformations</a>



<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>
 

 

