---
UID: NF:faxcomex.IFaxAccounts.get_Item
title: IFaxAccounts::get_Item (faxcomex.h)
description: Returns a FaxAccount object from a FaxAccounts collection.
helpviewer_keywords: ["IFaxAccounts interface [Fax Service]","get_Item method","IFaxAccounts.get_Item","IFaxAccounts::get_Item","_mfax_faxaccounts.item_cpp","fax._mfax_faxaccounts_item_cpp","faxcomex/IFaxAccounts::get_Item","get_Item","get_Item method [Fax Service]","get_Item method [Fax Service]","IFaxAccounts interface"]
old-location: fax\_mfax_faxaccounts_item_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxaccounts\get_item.htm
ms.date: 12/05/2018
ms.keywords: IFaxAccounts interface [Fax Service],get_Item method, IFaxAccounts.get_Item, IFaxAccounts::get_Item, _mfax_faxaccounts.item_cpp, fax._mfax_faxaccounts_item_cpp, faxcomex/IFaxAccounts::get_Item, get_Item, get_Item method [Fax Service], get_Item method [Fax Service],IFaxAccounts interface
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
 - IFaxAccounts::get_Item
 - faxcomex/IFaxAccounts::get_Item
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
 - IFaxAccounts.get_Item
---

# IFaxAccounts::get_Item


## -description

Returns a <a href="/previous-versions/windows/desktop/fax/-mfax-faxaccount">FaxAccount</a> object from a <a href="/previous-versions/windows/desktop/fax/-mfax-faxaccounts">FaxAccounts</a> collection.

## -parameters

### -param vIndex [in]

Type: <b>VARIANT</b>

<b>VARIANT</b> that specifies a value that indicates the item to retrieve from the collection. If this parameter is type <b>VT_I2</b> or <b>VT_I4</b>, it specifies the index of the item to retrieve. The index is 1-based. If this parameter is type <b>VT_BSTR</b>, it specifies the account name to use to search the collection. Other types are not supported.

### -param pFaxAccount [out, retval]

Type: <b><a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxaccount">IFaxAccount</a>**</b>

The <a href="/previous-versions/windows/desktop/fax/-mfax-faxaccount">FaxAccount</a> object.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxaccounts">IFaxAccounts</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-faxaccounts-item">Item</a>