---
UID: NN:certenroll.ICertificationAuthorities
title: ICertificationAuthorities
author: windows-driver-content
description: The ICertificationAuthorities interface defines the following methods and properties that manage a collection of ICertificationAuthority objects.
old-location: security\icertificationauthorities.htm
old-project: SecCertEnroll
ms.assetid: 8dad280a-1fe7-4a4b-9392-eee3aa9bcde9
ms.author: windowsdriverdev
ms.date: 4/5/2018
ms.keywords: ICertificationAuthorities, ICertificationAuthorities interface [Security], ICertificationAuthorities interface [Security], described, certenroll/ICertificationAuthorities, security.icertificationauthorities
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: certenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: CertEnroll.dll
req.typenames: X509RequestType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	CertEnroll.dll
api_name:
-	ICertificationAuthorities
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# ICertificationAuthorities interface


## -description


The  <b>ICertificationAuthorities</b> interface defines the following methods and properties that manage a collection of <a href="https://msdn.microsoft.com/ffd64396-a258-4cf5-aca1-a61102ecf313">ICertificationAuthority</a> objects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICertificationAuthorities</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>ICertificationAuthorities</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>ICertificationAuthorities</b> interface has these methods.
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
Adds an <a href="https://msdn.microsoft.com/ffd64396-a258-4cf5-aca1-a61102ecf313">ICertificationAuthority</a> object to the collection.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh406339">Clear</a>
</td>
<td align="left" width="63%">
Removes all <a href="https://msdn.microsoft.com/ffd64396-a258-4cf5-aca1-a61102ecf313">ICertificationAuthority</a> objects from the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8dae92da-e4b9-4512-b4f4-463b5a92a0d1">ComputeSiteCosts</a>
</td>
<td align="left" width="63%">
Not currently used.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439492">Remove</a>
</td>
<td align="left" width="63%">
Removes an <a href="https://msdn.microsoft.com/ffd64396-a258-4cf5-aca1-a61102ecf313">ICertificationAuthority</a> object from the collection by index number.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICertificationAuthorities</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/hh439300">_NewEnum</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the enumerator for the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/hh406342">Count</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the number of <a href="https://msdn.microsoft.com/ffd64396-a258-4cf5-aca1-a61102ecf313">ICertificationAuthority</a> objects in the collection.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/cc03b30c-0b61-4bf1-a688-c088e8420736">ItemByIndex</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves an <a href="https://msdn.microsoft.com/ffd64396-a258-4cf5-aca1-a61102ecf313">ICertificationAuthority</a> object from the collection by index number.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/90d620d6-1060-46fc-b593-9cb819b4eac8">ItemByName</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves an <a href="https://msdn.microsoft.com/ffd64396-a258-4cf5-aca1-a61102ecf313">ICertificationAuthority</a> object from the collection by certification authority name.

[WebEnabled]

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/ffd64396-a258-4cf5-aca1-a61102ecf313">ICertificationAuthority</a>



<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>
 

 

