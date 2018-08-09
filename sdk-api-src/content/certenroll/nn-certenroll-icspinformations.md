---
UID: NN:certenroll.ICspInformations
title: ICspInformations
author: windows-sdk-content
description: The ICspInformations interface defines the following methods and properties to manage a collection of ICspInformation objects.
old-location: security\icspinformations.htm
old-project: seccertenroll
ms.assetid: 8141023c-c162-46d6-9c37-e227ce1c8761
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: ICspInformations, ICspInformations interface [Security], ICspInformations interface [Security],described, certenroll/ICspInformations, security.icspinformations
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
tech.root: 
req.typenames: X509RequestType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - ICspInformations
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# ICspInformations interface


## -description


The <b>ICspInformations</b> interface defines the following methods and properties to manage a collection of <a href="https://msdn.microsoft.com/e337ae2c-6f86-4025-8d31-47bc5d8a4ca8">ICspInformation</a> objects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICspInformations</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>ICspInformations</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>ICspInformations</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn938485">Add</a>
</td>
<td align="left" width="63%">
Adds an <a href="https://msdn.microsoft.com/e337ae2c-6f86-4025-8d31-47bc5d8a4ca8">ICspInformation</a> object to the collection.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f44af323-41fb-46d6-88ed-15d465fc8815">AddAvailableCsps</a>
</td>
<td align="left" width="63%">
Adds the providers installed on the computer to the collection.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh406339">Clear</a>
</td>
<td align="left" width="63%">
Removes all <a href="https://msdn.microsoft.com/e337ae2c-6f86-4025-8d31-47bc5d8a4ca8">ICspInformation</a> objects from the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7c099357-8299-4664-ba16-7f8936e16054">GetCspStatusesFromOperations</a>
</td>
<td align="left" width="63%">
Retrieves an <a href="https://msdn.microsoft.com/73d0f3a7-7afd-42c9-88db-911531c50137">ICspStatuses</a> collection by supported key operations and optional provider information.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f73d40cb-dde3-46a5-ba9f-f7cbfa2efe70">GetCspStatusFromProviderName</a>
</td>
<td align="left" width="63%">
Retrieves an <a href="https://msdn.microsoft.com/30cc43c8-6ef3-49ad-8cff-9a5b7389ff68">ICspStatus</a> object for a legacy provider by provider name and supported key operations.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/85d2507c-0d0c-47a3-beb9-62af42b3ca3f">GetEncryptionCspAlgorithms</a>
</td>
<td align="left" width="63%">
Retrieves the  collection of encryption algorithms supported by a provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/647cad18-ed2e-4f3a-92d4-28fcfe60a800">GetHashAlgorithms</a>
</td>
<td align="left" width="63%">
Retrieves the collection of hash algorithms supported by a provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439492">Remove</a>
</td>
<td align="left" width="63%">
Removes an <a href="https://msdn.microsoft.com/e337ae2c-6f86-4025-8d31-47bc5d8a4ca8">ICspInformation</a> object from the collection by index number.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICspInformations</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/hh439300">_NewEnum</a>


</td>
<td align="left" width="63%">
Retrieves the enumerator for the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/hh406342">Count</a>


</td>
<td align="left" width="63%">
Retrieves the number of <a href="https://msdn.microsoft.com/e337ae2c-6f86-4025-8d31-47bc5d8a4ca8">ICspInformation</a> objects in the collection.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/9891dc5d-ebd6-4347-b47b-2def9c2d28a4">ItemByIndex</a>


</td>
<td align="left" width="63%">
Retrieves an <a href="https://msdn.microsoft.com/e337ae2c-6f86-4025-8d31-47bc5d8a4ca8">ICspInformation</a> object from the collection by index number.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/cf90f136-0318-40b5-9378-5c6f386e996f">ItemByName</a>


</td>
<td align="left" width="63%">
Retrieves an <a href="https://msdn.microsoft.com/e337ae2c-6f86-4025-8d31-47bc5d8a4ca8">ICspInformation</a> object from the collection by name.

[WebEnabled]

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/d49511ed-8651-457e-a102-0bea4edde24c">CertEnroll Interfaces</a>



<a href="https://msdn.microsoft.com/e337ae2c-6f86-4025-8d31-47bc5d8a4ca8">ICspInformation</a>



<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>
 

 

