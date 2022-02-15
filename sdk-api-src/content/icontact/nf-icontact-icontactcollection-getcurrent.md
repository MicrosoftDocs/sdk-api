---
UID: NF:icontact.IContactCollection.GetCurrent
title: IContactCollection::GetCurrent (icontact.h)
description: Retrieves the current contact in the enumeration.
helpviewer_keywords: ["GetCurrent","GetCurrent method [Windows Contacts]","GetCurrent method [Windows Contacts]","IContactCollection interface","IContactCollection interface [Windows Contacts]","GetCurrent method","IContactCollection.GetCurrent","IContactCollection::GetCurrent","_wincontacts_IContactCollection_GetCurrent","icontact/IContactCollection::GetCurrent","wincontacts._wincontacts_IContactCollection_GetCurrent"]
old-location: wincontacts\_wincontacts_IContactCollection_GetCurrent.htm
tech.root: wincontacts
ms.assetid: e5a5d27d-121a-4755-892e-53d148facd74
ms.date: 12/05/2018
ms.keywords: GetCurrent, GetCurrent method [Windows Contacts], GetCurrent method [Windows Contacts],IContactCollection interface, IContactCollection interface [Windows Contacts],GetCurrent method, IContactCollection.GetCurrent, IContactCollection::GetCurrent, _wincontacts_IContactCollection_GetCurrent, icontact/IContactCollection::GetCurrent, wincontacts._wincontacts_IContactCollection_GetCurrent
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
 - IContactCollection::GetCurrent
 - icontact/IContactCollection::GetCurrent
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
 - IContactCollection.GetCurrent
---

# IContactCollection::GetCurrent


## -description

Retrieves the current contact in the enumeration.

## -parameters

### -param ppContact [out]

Type: <b><a href="/previous-versions/windows/desktop/api/icontact/nn-icontact-icontact">IContact</a>**</b>

If successful, contains the current contact.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

After reset, a call to <b>IContactCollection::GetCurrent</b> without first calling <a href="/previous-versions/windows/desktop/api/icontact/nf-icontact-icontactcollection-next">IContactCollection::Next</a> will fail.

## -see-also

<a href="/previous-versions/windows/desktop/api/icontact/nn-icontact-icontactcollection">IContactCollection</a>



<a href="/previous-versions/windows/desktop/api/icontact/nf-icontact-icontactcollection-reset">IContactCollection::Reset</a>