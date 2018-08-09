---
UID: NN:azroles.IAzApplications
title: IAzApplications
author: windows-sdk-content
description: Represents a collection of IAzApplication objects.
old-location: security\iazapplications.htm
old-project: secauthz
ms.assetid: 04cee21c-253a-463a-9231-592ddad88188
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IAzApplications, IAzApplications interface [Security], IAzApplications interface [Security],described, azroles/IAzApplications, security.iazapplications
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: azroles.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: AZ_PROP_CONSTANTS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Azroles.dll
api_name:
 - IAzApplications
product: Windows
targetos: Windows
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
---

# IAzApplications interface


## -description


The <b>IAzApplications</b> interface represents a collection of  
<a href="https://msdn.microsoft.com/ea4a8a84-5003-44da-b75e-34da6bd898dd">IAzApplication</a> objects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAzApplications</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IAzApplications</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IAzApplications</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8c01c1b4-d3e0-40c2-b0b7-524423c38c45">get__NewEnum</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://msdn.microsoft.com/library/windows/hardware/hh439300">_NewEnum</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2f12fd9f-4632-4eef-8ac4-80e73a731539">get_Count</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://msdn.microsoft.com/library/windows/hardware/hh406342">Count</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a5d6edd2-d93d-4168-89b8-6dbe60e3d4b9">get_Item</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://msdn.microsoft.com/library/windows/hardware/hh451057">Item</a> property.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAzApplications</b> interface has these properties.
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
Retrieves an <a href="https://msdn.microsoft.com/en-us/library/ms221053(v=VS.85).aspx">IEnumVARIANT</a> interface on an object that can be used to enumerate the collection. This property is hidden within Visual Basic and Visual Basic Scripting Edition (VBScript).

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
Retrieves the number of <a href="https://msdn.microsoft.com/ea4a8a84-5003-44da-b75e-34da6bd898dd">IAzApplication</a> objects in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/hh451057">Item</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the <a href="https://msdn.microsoft.com/ea4a8a84-5003-44da-b75e-34da6bd898dd">IAzApplication</a> object at the specified index into the <b>IAzApplications</b> collection.

</td>
</tr>
</table> 

