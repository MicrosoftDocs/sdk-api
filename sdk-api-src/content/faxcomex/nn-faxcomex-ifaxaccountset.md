---
UID: NN:faxcomex.IFaxAccountSet
title: IFaxAccountSet
author: windows-sdk-content
description: Provides methods for fax account management, including adding, removing, and retrieving fax accounts.
old-location: fax\_mfax_faxaccountset_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxaccountset\faxinta_n_ifaxaccountset.htm
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: IFaxAccountSet, IFaxAccountSet interface [Fax Service], IFaxAccountSet interface [Fax Service],described, _mfax_faxaccountset_cpp, fax._mfax_faxaccountset_cpp, faxcomex/IFaxAccountSet
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
 - IFaxAccountSet
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxAccountSet interface


## -description


Provides methods for <a href="https://msdn.microsoft.com/ede1c31f-e53a-4ddc-ba25-6fcadadd513a">fax account</a> management, including adding, removing, and retrieving fax accounts. 
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxAccountSet</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IFaxAccountSet</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/0d9093b3-4c30-409d-b2f0-dbb87f5b009b">AddAccount</a>
</td>
<td align="left" width="63%">
Adds a fax account to the fax server and returns the new <a href="https://msdn.microsoft.com/438a35bd-d08b-4b29-95e5-81ff5c23e92b">IFaxAccount</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ccb844f1-fb6b-45dd-a1e6-cd4a0643a3fb">GetAccount</a>
</td>
<td align="left" width="63%">
Returns an <a href="https://msdn.microsoft.com/438a35bd-d08b-4b29-95e5-81ff5c23e92b">IFaxAccount</a> object by using the account name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c55ddf0c-9aef-4999-ba20-8da34afad311">GetAccounts</a>
</td>
<td align="left" width="63%">
Returns an <a href="https://msdn.microsoft.com/73210bf5-cae8-4fea-802a-a37f59a1dd2f">IFaxAccounts</a> object that represents all the fax accounts on the fax server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c61e8fe5-d4f0-4e47-91af-05799208f8fd">RemoveAccount</a>
</td>
<td align="left" width="63%">
Removes a fax account from the fax server.

</td>
</tr>
</table> 


## -remarks



A default implementation of <b>IFaxAccountSet</b> is provided as the <a href="https://msdn.microsoft.com/ae298925-c428-420e-a0a2-ce3f72c5cff4">FaxAccountSet</a> object. The interface and the object are supported only on Windows Vista or later.



