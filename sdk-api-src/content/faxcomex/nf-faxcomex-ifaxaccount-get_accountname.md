---
UID: NF:faxcomex.IFaxAccount.get_AccountName
title: IFaxAccount::get_AccountName (faxcomex.h)
description: Retrieves the name of a particular fax account on the server.
helpviewer_keywords: ["AccountName property [Fax Service]","AccountName property [Fax Service]","IFaxAccount interface","IFaxAccount interface [Fax Service]","AccountName property","IFaxAccount.AccountName","IFaxAccount.get_AccountName","IFaxAccount::AccountName","IFaxAccount::get_AccountName","_mfax_faxaccount.accountname","fax._mfax_faxaccount_accountname","fax._mfax_faxaccount_cpp_mfax_faxaccount_accountname_cpp","faxcomex/IFaxAccount::AccountName","faxcomex/IFaxAccount::get_AccountName","get_AccountName"]
old-location: fax\_mfax_faxaccount_cpp_mfax_faxaccount_accountname_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxaccount\accountname.htm
ms.date: 12/05/2018
ms.keywords: AccountName property [Fax Service], AccountName property [Fax Service],IFaxAccount interface, IFaxAccount interface [Fax Service],AccountName property, IFaxAccount.AccountName, IFaxAccount.get_AccountName, IFaxAccount::AccountName, IFaxAccount::get_AccountName, _mfax_faxaccount.accountname, fax._mfax_faxaccount_accountname, fax._mfax_faxaccount_cpp_mfax_faxaccount_accountname_cpp, faxcomex/IFaxAccount::AccountName, faxcomex/IFaxAccount::get_AccountName, get_AccountName
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFaxAccount::get_AccountName
 - faxcomex/IFaxAccount::get_AccountName
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fxscomex.dll
api_name:
 - IFaxAccount.AccountName
 - IFaxAccount.get_AccountName
---

# IFaxAccount::get_AccountName


## -description

Retrieves the name of a particular fax account on the server.

This property is read-only.

## -parameters

## -remarks

If the account is not in the local domain, the format of name returned  is &lt;domain_name&gt;\&lt;user_name&gt;.

If the account is in the domain but not on the server, the format name returned is &lt;computer_name&gt;\&lt;user_name&gt; where &lt;computer_name&gt; is the name of the server that holds the account.

If the account is on the same server as the fax server, just the &lt;user_name&gt; of the account is returned.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxaccount">FaxAccount</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxaccount">IFaxAccount</a>