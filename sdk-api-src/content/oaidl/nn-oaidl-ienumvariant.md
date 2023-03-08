---
UID: NN:oaidl.IEnumVARIANT
title: IEnumVARIANT (oaidl.h)
description: Provides a method for enumerating a collection of variants, including heterogeneous collections of objects and intrinsic types.
helpviewer_keywords: ["IEnumVARIANT","IEnumVARIANT interface [Automation]","IEnumVARIANT interface [Automation]","described","_oa96_IEnumVARIANT_Interface","automat.ienumvariant","oaidl/IEnumVARIANT"]
old-location: automat\ienumvariant.htm
tech.root: automat
ms.assetid: 139e3c93-faef-4003-9079-e0e94494db3e
ms.date: 12/05/2018
ms.keywords: IEnumVARIANT, IEnumVARIANT interface [Automation], IEnumVARIANT interface [Automation],described, _oa96_IEnumVARIANT_Interface, automat.ienumvariant, oaidl/IEnumVARIANT
req.header: oaidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OaIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEnumVARIANT
 - oaidl/IEnumVARIANT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - stdole.dll
api_name:
 - IEnumVARIANT
---

# IEnumVARIANT interface


## -description

Provides a method for enumerating a collection of variants, including heterogeneous collections of objects and intrinsic types. Callers of this interface do not need to know the specific type (or types) of the elements in the collection.

## -inheritance

The <b>IEnumVARIANT</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumVARIANT</b> also has these types of members:

## -remarks

To see how to implement a collection of objects using <b>IEnumVARIANT</b>, refer to the file Enumvar.cpp in the Lines sample code.
