---
UID: NF:icontact.IContactCollection.Reset
title: IContactCollection::Reset (icontact.h)
description: Resets the enumerator to before the logical first element.
helpviewer_keywords: ["IContactCollection interface [Windows Contacts]","Reset method","IContactCollection.Reset","IContactCollection::Reset","Reset","Reset method [Windows Contacts]","Reset method [Windows Contacts]","IContactCollection interface","_wincontacts_IContactCollection_Reset","icontact/IContactCollection::Reset","wincontacts._wincontacts_IContactCollection_Reset"]
old-location: wincontacts\_wincontacts_IContactCollection_Reset.htm
tech.root: wincontacts
ms.assetid: 31922d03-079e-4a6f-8516-d4cf540d812e
ms.date: 12/05/2018
ms.keywords: IContactCollection interface [Windows Contacts],Reset method, IContactCollection.Reset, IContactCollection::Reset, Reset, Reset method [Windows Contacts], Reset method [Windows Contacts],IContactCollection interface, _wincontacts_IContactCollection_Reset, icontact/IContactCollection::Reset, wincontacts._wincontacts_IContactCollection_Reset
req.header: icontact.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Icontact.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Wab32.dll (Version 6.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IContactCollection::Reset
 - icontact/IContactCollection::Reset
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wab32.dll
api_name:
 - IContactCollection.Reset
---

# IContactCollection::Reset


## -description

Resets the enumerator to before the logical first element.



## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

A call to <a href="/previous-versions/windows/desktop/api/icontact/nf-icontact-icontactcollection-getcurrent">IContactCollection::GetCurrent</a> immediately after <b>IContactCollection::Reset</b> is undefined. To get the first contact, call <a href="/previous-versions/windows/desktop/api/icontact/nf-icontact-icontactcollection-next">IContactCollection::Next</a> first to ensure that there is one.
