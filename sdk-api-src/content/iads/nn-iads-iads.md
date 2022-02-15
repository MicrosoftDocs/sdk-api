---
UID: NN:iads.IADs
title: IADs (iads.h)
description: The IADs interface defines the basic object features, that is, properties and methods, of any ADSI object.
helpviewer_keywords: ["IADs","IADs interface [ADSI]","IADs interface [ADSI]","described","_ds_iads","adsi.iads","iads/IADs"]
old-location: adsi\iads.htm
tech.root: adsi
ms.assetid: f53d9ee0-3f4d-4a01-b953-98d168ad94cb
ms.date: 12/05/2018
ms.keywords: IADs, IADs interface [ADSI], IADs interface [ADSI],described, _ds_iads, adsi.iads, iads/IADs
req.header: iads.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.dll: Activeds.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IADs
 - iads/IADs
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Activeds.dll
api_name:
 - IADs
---

# IADs interface


## -description

The <b>IADs</b> interface defines the basic object features, that is, properties and methods, of any ADSI object. Examples of ADSI objects include users, computers, services, organization of user accounts and computers, file systems, and file service operations. Every ADSI object must support this interface, which serves to do the following:
<ul>
<li>Provides object identification by name, class, or ADsPath</li>
<li>Identifies the object's container that manages the object's creation and deletion</li>
<li>Retrieves the object's schema definition</li>
<li>Loads object's attributes to the property cache and commits changes to the persistent directory store</li>
<li>Accesses and modifies the object's attribute values in the property cache</li>
</ul>The <b>IADs</b> interface is designed to ensure that ADSI objects provide network administrators and directory service providers with a simple and consistent representation of various underlying directory services.

## -inheritance

The <b>IADs</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IADs</b> also has these types of members:

