---
UID: NF:faxcomex.IFaxAccountSet.AddAccount
title: IFaxAccountSet::AddAccount (faxcomex.h)
description: Adds a fax account to the fax server and returns the new IFaxAccount object.
helpviewer_keywords: ["AddAccount","AddAccount method [Fax Service]","AddAccount method [Fax Service]","IFaxAccountSet interface","IFaxAccountSet interface [Fax Service]","AddAccount method","IFaxAccountSet.AddAccount","IFaxAccountSet::AddAccount","_mfax_faxaccountset.addaccount","fax._mfax_faxaccountset_addaccount","fax._mfax_faxaccountset_cpp_mfax_faxaccountset_addaccount_cpp","faxcomex/IFaxAccountSet::AddAccount"]
old-location: fax\_mfax_faxaccountset_cpp_mfax_faxaccountset_addaccount_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxaccountset\addaccount.htm
ms.date: 12/05/2018
ms.keywords: AddAccount, AddAccount method [Fax Service], AddAccount method [Fax Service],IFaxAccountSet interface, IFaxAccountSet interface [Fax Service],AddAccount method, IFaxAccountSet.AddAccount, IFaxAccountSet::AddAccount, _mfax_faxaccountset.addaccount, fax._mfax_faxaccountset_addaccount, fax._mfax_faxaccountset_cpp_mfax_faxaccountset_addaccount_cpp, faxcomex/IFaxAccountSet::AddAccount
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
 - IFaxAccountSet::AddAccount
 - faxcomex/IFaxAccountSet::AddAccount
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
 - IFaxAccountSet.AddAccount
---

# IFaxAccountSet::AddAccount


## -description

Adds a fax account to the fax server and returns the new <a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxaccount">IFaxAccount</a> object.

## -parameters

### -param bstrAccountName [in]

Type: <b>BSTR</b>

Specifies a null-terminated string that contains a name for the new account.

### -param pFaxAccount

Type: <b><a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxaccount">IFaxAccount</a>**</b>

The address of a pointer to an <a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxaccount">IFaxAccount</a> object.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<i>bstrAccountName</i> must be of the form &lt;domainName&gt;\&lt;username&gt; or just &lt;username&gt; for local users.

When the new account is returned, all its values except the name are set to defaults.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxaccountset">FaxAccountSet</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxaccountset">IFaxAccountSet</a>