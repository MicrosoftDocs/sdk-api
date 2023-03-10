---
UID: NF:comsvcs.IObjectConstructString.get_ConstructString
title: IObjectConstructString::get_ConstructString (comsvcs.h)
description: Retrieves the constructor string for the object.
helpviewer_keywords: ["IObjectConstructString interface [COM+]","get_ConstructString method","IObjectConstructString.get_ConstructString","IObjectConstructString::get_ConstructString","_cos_IObjectConstructString_get_ConstructString","comsvcs/IObjectConstructString::get_ConstructString","cos.iobjectconstructstring_get_constructstring","get_ConstructString","get_ConstructString method [COM+]","get_ConstructString method [COM+]","IObjectConstructString interface"]
old-location: cos\iobjectconstructstring_get_constructstring.htm
tech.root: cos
ms.assetid: 154b7567-0f25-49c3-90b2-58c95f0ebfee
ms.date: 12/05/2018
ms.keywords: IObjectConstructString interface [COM+],get_ConstructString method, IObjectConstructString.get_ConstructString, IObjectConstructString::get_ConstructString, _cos_IObjectConstructString_get_ConstructString, comsvcs/IObjectConstructString::get_ConstructString, cos.iobjectconstructstring_get_constructstring, get_ConstructString, get_ConstructString method [COM+], get_ConstructString method [COM+],IObjectConstructString interface
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IObjectConstructString::get_ConstructString
 - comsvcs/IObjectConstructString::get_ConstructString
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IObjectConstructString.get_ConstructString
---

# IObjectConstructString::get_ConstructString


## -description

Retrieves the constructor string for the object.

Object constructor strings should not be used to store security-sensitive information.

## -parameters

### -param pVal [out]

A reference to an administratively supplied object constructor string.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -remarks

You can use this method when implementing <a href="/windows/desktop/api/comsvcs/nf-comsvcs-iobjectconstruct-construct">IObjectConstruct::Construct</a>, which is called by the COM+ environment when your component is marked as supporting object construction.

## -see-also

<a href="/windows/desktop/cossdk/com--object-constructor-strings">COM+ Object Constructor Strings</a>



<a href="/windows/desktop/api/comsvcs/nn-comsvcs-iobjectconstruct">IObjectConstruct</a>



<a href="/windows/desktop/api/comsvcs/nn-comsvcs-iobjectconstructstring">IObjectConstructString</a>



<a href="/windows/desktop/cossdk/specifying-an-object-constructor-string-for-a-component">Specifying an Object Constructor String for a Component</a>