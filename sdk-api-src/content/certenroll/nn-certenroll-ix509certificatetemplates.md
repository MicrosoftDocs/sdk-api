---
UID: NN:certenroll.IX509CertificateTemplates
title: IX509CertificateTemplates
author: windows-sdk-content
description: The IX509CertificateTemplates interface defines the following methods and properties that manage a collection of IX509CertificateTemplate objects.
old-location: security\ix509certificatetemplates.htm
tech.root: SecCertEnroll
ms.assetid: 82d14b93-e07b-4ff3-88b9-b1873972b4ad
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IX509CertificateTemplates, IX509CertificateTemplates interface [Security], IX509CertificateTemplates interface [Security],described, certenroll/IX509CertificateTemplates, security.ix509certificatetemplates
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - IX509CertificateTemplates
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509CertificateTemplates interface


## -description


The <b>IX509CertificateTemplates</b> interface defines the following methods and properties that manage a collection of <a href="https://msdn.microsoft.com/en-us/library/Ee351664(v=VS.85).aspx">IX509CertificateTemplate</a> objects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509CertificateTemplates</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IX509CertificateTemplates</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Properties</a></li>
</ul>

## -members

The <b>IX509CertificateTemplates</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ee351667(v=VS.85).aspx">Add</a>
</td>
<td align="left" width="63%">
Adds an <a href="https://msdn.microsoft.com/en-us/library/Ee351664(v=VS.85).aspx">IX509CertificateTemplate</a> object to the collection.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ee351668(v=VS.85).aspx">Clear</a>
</td>
<td align="left" width="63%">
Removes all <a href="https://msdn.microsoft.com/en-us/library/Ee351664(v=VS.85).aspx">IX509CertificateTemplate</a> objects from the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ee351673(v=VS.85).aspx">Remove</a>
</td>
<td align="left" width="63%">
Removes an <a href="https://msdn.microsoft.com/en-us/library/Ee351664(v=VS.85).aspx">IX509CertificateTemplate</a> object from the collection by index number.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509CertificateTemplates</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Ee351674(v=VS.85).aspx">_NewEnum</a>


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

<a href="https://msdn.microsoft.com/en-us/library/Ee351669(v=VS.85).aspx">Count</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the number of <a href="https://msdn.microsoft.com/en-us/library/Ee351664(v=VS.85).aspx">IX509CertificateTemplate</a> objects in the collection.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/1d7ddfd8-89f4-485a-ba90-83f2331168d2">ItemByIndex</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves an <a href="https://msdn.microsoft.com/en-us/library/Ee351664(v=VS.85).aspx">IX509CertificateTemplate</a> object from the collection by index number.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Ee351671(v=VS.85).aspx">ItemByName</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves an <a href="https://msdn.microsoft.com/en-us/library/Ee351664(v=VS.85).aspx">IX509CertificateTemplate</a> object from the collection by name.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Ee351672(v=VS.85).aspx">ItemByOid</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves an <a href="https://msdn.microsoft.com/en-us/library/Ee351664(v=VS.85).aspx">IX509CertificateTemplate</a> object from the collection by <a href="https://msdn.microsoft.com/en-us/library/ms721599(v=VS.85).aspx">object identifier</a>.

</td>
</tr>
</table> 

