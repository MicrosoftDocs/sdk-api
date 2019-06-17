---
UID: NN:faxcomex.IFaxAccountSet
title: IFaxAccountSet (faxcomex.h)
author: windows-sdk-content
description: Provides methods for fax account management, including adding, removing, and retrieving fax accounts.
old-location: fax\_mfax_faxaccountset_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxaccountset\faxinta_n_ifaxaccountset.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IFaxAccountSet, IFaxAccountSet interface [Fax Service], IFaxAccountSet interface [Fax Service],described, _mfax_faxaccountset_cpp, fax._mfax_faxaccountset_cpp, faxcomex/IFaxAccountSet
ms.topic: interface
f1_keywords: ["faxcomex/IFaxAccountSet"]
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
 - IFaxAccountSet
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFaxAccountSet interface


## -description


Provides methods for <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-glossary">fax account</a> management, including adding, removing, and retrieving fax accounts. 
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxAccountSet</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IFaxAccountSet</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFaxAccountSet</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxaccountset-addaccount-vb">AddAccount</a>
</td>
<td align="left" width="63%">
Adds a fax account to the fax server and returns the new <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxaccount">IFaxAccount</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxaccountset-getaccount-vb">GetAccount</a>
</td>
<td align="left" width="63%">
Returns an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxaccount">IFaxAccount</a> object by using the account name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxaccountset-getaccounts-vb">GetAccounts</a>
</td>
<td align="left" width="63%">
Returns an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxaccounts">IFaxAccounts</a> object that represents all the fax accounts on the fax server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxaccountset-removeaccount-vb">RemoveAccount</a>
</td>
<td align="left" width="63%">
Removes a fax account from the fax server.

</td>
</tr>
</table> 


## -remarks



A default implementation of <b>IFaxAccountSet</b> is provided as the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxaccountset">FaxAccountSet</a> object. The interface and the object are supported only on Windows Vista or later.



