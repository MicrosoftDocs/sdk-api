---
UID: NF:propsys.IPropertyChangeArray.Append
title: IPropertyChangeArray::Append (propsys.h)
description: Inserts a change operation at the end of an array.
old-location: properties\IPropertyChangeArray_Append.htm
tech.root: properties
ms.assetid: 45039163-dffc-4168-9c31-786dcfdab760
ms.date: 12/05/2018
ms.keywords: Append, Append method [Windows Properties], Append method [Windows Properties],IPropertyChangeArray interface, IPropertyChangeArray interface [Windows Properties],Append method, IPropertyChangeArray.Append, IPropertyChangeArray::Append, _shell_IPropertyChangeArray_Append, properties.IPropertyChangeArray_Append, propsys/IPropertyChangeArray::Append, shell.IPropertyChangeArray_Append
ms.topic: method
f1_keywords:
- propsys/IPropertyChangeArray.Append
dev_langs:
- c++
req.header: propsys.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Propsys.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Propsys.h
api_name:
- IPropertyChangeArray.Append
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPropertyChangeArray::Append


## -description


Inserts a change operation at the end of an array.


## -parameters




### -param ppropChange [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/propsys/nn-propsys-ipropertychange">IPropertyChange</a>*</b>

A pointer to the interface that contains the change.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



