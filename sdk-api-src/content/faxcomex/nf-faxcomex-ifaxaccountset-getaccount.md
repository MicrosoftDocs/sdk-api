---
UID: NF:faxcomex.IFaxAccountSet.GetAccount
title: IFaxAccountSet::GetAccount (faxcomex.h)
description: Returns an IFaxAccount object by using the account name.
helpviewer_keywords: ["GetAccount","GetAccount method [Fax Service]","GetAccount method [Fax Service]","IFaxAccountSet interface","IFaxAccountSet interface [Fax Service]","GetAccount method","IFaxAccountSet.GetAccount","IFaxAccountSet::GetAccount","_mfax_faxaccountset.getaccount","fax._mfax_faxaccountset_cpp_mfax_faxaccountset_getaccount_cpp","fax._mfax_faxaccountset_getaccount","faxcomex/IFaxAccountSet::GetAccount"]
old-location: fax\_mfax_faxaccountset_cpp_mfax_faxaccountset_getaccount_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxaccountset\getaccount.htm
ms.date: 12/05/2018
ms.keywords: GetAccount, GetAccount method [Fax Service], GetAccount method [Fax Service],IFaxAccountSet interface, IFaxAccountSet interface [Fax Service],GetAccount method, IFaxAccountSet.GetAccount, IFaxAccountSet::GetAccount, _mfax_faxaccountset.getaccount, fax._mfax_faxaccountset_cpp_mfax_faxaccountset_getaccount_cpp, fax._mfax_faxaccountset_getaccount, faxcomex/IFaxAccountSet::GetAccount
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
 - IFaxAccountSet::GetAccount
 - faxcomex/IFaxAccountSet::GetAccount
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
 - IFaxAccountSet.GetAccount
 - IFaxAccountSet.GetAccount
---

# IFaxAccountSet::GetAccount


## -description

Returns an <a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxaccount">IFaxAccount</a> object by using the account name.

## -parameters

### -param bstrAccountName [in]

Type: <b>BSTR</b>

Specifies a null-terminated string that contains the name of the account to return.

### -param pFaxAccount

Type: <b><a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxaccount">IFaxAccount</a>**</b>

The address of a pointer to an <a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxaccount">IFaxAccount</a> object.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<i>bstrAccountName</i> must be of the form &lt;domainName&gt;\&lt;username&gt; or just &lt;username&gt; for local users.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxaccountset">FaxAccountSet</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxaccountset">IFaxAccountSet</a>