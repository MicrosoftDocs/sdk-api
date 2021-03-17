---
UID: NF:comsvcs.IGetContextProperties.EnumNames
title: IGetContextProperties::EnumNames (comsvcs.h)
description: Retrieves a list of the names of the current context properties.
helpviewer_keywords: ["EnumNames","EnumNames method [COM+]","EnumNames method [COM+]","IGetContextProperties interface","IGetContextProperties interface [COM+]","EnumNames method","IGetContextProperties.EnumNames","IGetContextProperties::EnumNames","_cos_IGetContextProperties_EnumNames","comsvcs/IGetContextProperties::EnumNames","cos.igetcontextproperties_enumnames"]
old-location: cos\igetcontextproperties_enumnames.htm
tech.root: cos
ms.assetid: 01ff9650-f7f1-440c-88d2-75ba793a2396
ms.date: 12/05/2018
ms.keywords: EnumNames, EnumNames method [COM+], EnumNames method [COM+],IGetContextProperties interface, IGetContextProperties interface [COM+],EnumNames method, IGetContextProperties.EnumNames, IGetContextProperties::EnumNames, _cos_IGetContextProperties_EnumNames, comsvcs/IGetContextProperties::EnumNames, cos.igetcontextproperties_enumnames
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
 - IGetContextProperties::EnumNames
 - comsvcs/IGetContextProperties::EnumNames
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
 - IGetContextProperties.EnumNames
---

# IGetContextProperties::EnumNames


## -description

Retrieves a list of the names of the current context properties.

## -parameters

### -param ppenum [out, retval]

An <a href="/windows/desktop/api/comsvcs/nn-comsvcs-ienumnames">IEnumNames</a> interface providing access to a list of the names of the current context properties.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-igetcontextproperties">IGetContextProperties</a>