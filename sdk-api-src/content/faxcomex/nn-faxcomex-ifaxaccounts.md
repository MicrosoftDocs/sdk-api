---
UID: NN:faxcomex.IFaxAccounts
title: IFaxAccounts
author: windows-sdk-content
description: Represents the collection of fax accounts on the fax server. It provides methods and properties for enumerating the accounts, retrieving a particular account, and reporting the total number of accounts.
old-location: fax\_mfax_faxaccounts_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxaccounts\faxinta_n_ifaxaccounts.htm
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: IFaxAccounts, IFaxAccounts interface [Fax Service], IFaxAccounts interface [Fax Service],described, _mfax_faxaccounts_cpp, fax._mfax_faxaccounts_cpp, faxcomex/IFaxAccounts
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: faxcomex.h
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
req.dll: Fxscomex.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fxscomex.dll
api_name:
 - IFaxAccounts
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxAccounts interface


## -description


Represents the collection of fax accounts on the fax server. It provides methods and properties for enumerating the accounts, retrieving a particular account, and reporting the total number of accounts. 
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxAccounts</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IFaxAccounts</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IFaxAccounts</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bdbf117a-6855-4306-9572-5355fdccdfc3">get_Item</a>
</td>
<td align="left" width="63%">
Returns a <a href="https://msdn.microsoft.com/85adc440-3dc8-47ce-aae8-dfb04f824b09">FaxAccount</a> object from a <a href="https://msdn.microsoft.com/bf26e82e-af97-43a1-81be-1bcb61b6cf98">FaxAccounts</a> collection. 

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxAccounts</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/af926d20-fd72-4b9a-ba70-e3bf64eda3a4">Count</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Holds the number of items in the <b>IFaxAccounts</b> collection. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/90eebc3b-1113-4512-b08f-5d73df8b2d7f">NewEnum</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Holds the enumerator for the <b>IFaxAccounts</b> object. 

</td>
</tr>
</table> 


## -remarks



A default implementation of <b>IFaxAccounts</b> is provided as the <a href="https://msdn.microsoft.com/bf26e82e-af97-43a1-81be-1bcb61b6cf98">FaxAccounts</a> object. The interface and the object are supported only on Windows Vista or later.



