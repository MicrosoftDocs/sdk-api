---
UID: NF:faxcomex.IFaxAccountSet.GetAccounts
title: IFaxAccountSet::GetAccounts (faxcomex.h)
description: Returns an IFaxAccounts object that represents all the fax accounts on the fax server.
helpviewer_keywords: ["GetAccounts","GetAccounts method [Fax Service]","GetAccounts method [Fax Service]","IFaxAccountSet interface","IFaxAccountSet interface [Fax Service]","GetAccounts method","IFaxAccountSet.GetAccounts","IFaxAccountSet::GetAccounts","_mfax_faxaccountset.getaccounts","fax._mfax_faxaccountset_cpp_mfax_faxaccountset_getaccounts_cpp","fax._mfax_faxaccountset_getaccounts","faxcomex/IFaxAccountSet::GetAccounts"]
old-location: fax\_mfax_faxaccountset_cpp_mfax_faxaccountset_getaccounts_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxaccountset\getaccounts.htm
ms.date: 12/05/2018
ms.keywords: GetAccounts, GetAccounts method [Fax Service], GetAccounts method [Fax Service],IFaxAccountSet interface, IFaxAccountSet interface [Fax Service],GetAccounts method, IFaxAccountSet.GetAccounts, IFaxAccountSet::GetAccounts, _mfax_faxaccountset.getaccounts, fax._mfax_faxaccountset_cpp_mfax_faxaccountset_getaccounts_cpp, fax._mfax_faxaccountset_getaccounts, faxcomex/IFaxAccountSet::GetAccounts
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
 - IFaxAccountSet::GetAccounts
 - faxcomex/IFaxAccountSet::GetAccounts
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
 - IFaxAccountSet.GetAccounts
 - IFaxAccountSet.GetAccounts
---

# IFaxAccountSet::GetAccounts


## -description

Returns an <a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxaccounts">IFaxAccounts</a> object that represents all the fax accounts on the fax server.

## -parameters

### -param ppFaxAccounts [out, retval]

Type: <b><a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxaccounts">IFaxAccounts</a>**</b>

The address of a pointer to an <a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxaccounts">IFaxAccounts</a> object.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxaccountset">FaxAccountSet</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxaccountset">IFaxAccountSet</a>