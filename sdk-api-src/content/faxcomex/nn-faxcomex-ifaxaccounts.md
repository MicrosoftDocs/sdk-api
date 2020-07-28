---
UID: NN:faxcomex.IFaxAccounts
title: IFaxAccounts (faxcomex.h)
description: Represents the collection of fax accounts on the fax server. It provides methods and properties for enumerating the accounts, retrieving a particular account, and reporting the total number of accounts.
helpviewer_keywords: ["IFaxAccounts","IFaxAccounts interface [Fax Service]","IFaxAccounts interface [Fax Service]","described","_mfax_faxaccounts_cpp","fax._mfax_faxaccounts_cpp","faxcomex/IFaxAccounts"]
old-location: fax\_mfax_faxaccounts_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxaccounts\faxinta_n_ifaxaccounts.htm
ms.date: 12/05/2018
ms.keywords: IFaxAccounts, IFaxAccounts interface [Fax Service], IFaxAccounts interface [Fax Service],described, _mfax_faxaccounts_cpp, fax._mfax_faxaccounts_cpp, faxcomex/IFaxAccounts
f1_keywords:
- faxcomex/IFaxAccounts
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFaxAccounts interface


## -description


Represents the collection of fax accounts on the fax server. It provides methods and properties for enumerating the accounts, retrieving a particular account, and reporting the total number of accounts. 
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxAccounts</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IFaxAccounts</b> also has these types of members:
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nf-faxcomex-ifaxaccounts-get_item">get_Item</a>
</td>
<td align="left" width="63%">
Returns a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxaccount">FaxAccount</a> object from a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxaccounts">FaxAccounts</a> collection. 

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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxaccounts-count-vb">Count</a>


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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxaccounts-newenum-vb">NewEnum</a>


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



A default implementation of <b>IFaxAccounts</b> is provided as the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxaccounts">FaxAccounts</a> object. The interface and the object are supported only on Windows Vista or later.



