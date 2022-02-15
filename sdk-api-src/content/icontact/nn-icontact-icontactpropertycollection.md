---
UID: NN:icontact.IContactPropertyCollection
title: IContactPropertyCollection (icontact.h)
description: Do not use. Used to filter contact data, based on a label or property set. Enumerates contact properties exposed with an IContactProperties object. For each property, the name, type, version, and modification date can be retrieved.
helpviewer_keywords: ["IContactPropertyCollection","IContactPropertyCollection interface [Windows Contacts]","IContactPropertyCollection interface [Windows Contacts]","described","_wincontacts_IContactPropertyCollection","icontact/IContactPropertyCollection","wincontacts._wincontacts_IContactPropertyCollection"]
old-location: wincontacts\_wincontacts_IContactPropertyCollection.htm
tech.root: wincontacts
ms.assetid: dec9430d-2174-42fe-85c1-16fa7e7adc0c
ms.date: 12/05/2018
ms.keywords: IContactPropertyCollection, IContactPropertyCollection interface [Windows Contacts], IContactPropertyCollection interface [Windows Contacts],described, _wincontacts_IContactPropertyCollection, icontact/IContactPropertyCollection, wincontacts._wincontacts_IContactPropertyCollection
req.header: icontact.h
req.include-header: Contact.h
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
 - IContactPropertyCollection
 - icontact/IContactPropertyCollection
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
 - IContactPropertyCollection
---

# IContactPropertyCollection interface


## -description

Do not use. Used to filter contact data, based on a label or property set. Enumerates contact properties 
		exposed with an <a href="/previous-versions/windows/desktop/api/icontact/nn-icontact-icontactproperties">IContactProperties</a> object. For each property, 
		the name, type, version, and modification date can be retrieved.

## -inheritance

The <b>IContactPropertyCollection</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IContactPropertyCollection</b> also has these types of members:

## -remarks

<div class="alert"><b>Note</b>  Changing the <a href="/previous-versions/windows/desktop/api/icontact/nn-icontact-icontactproperties">IContactProperties</a> properties object 
		while enumerating properties with this interface results in undefined behavior.</div>
<div> </div>
