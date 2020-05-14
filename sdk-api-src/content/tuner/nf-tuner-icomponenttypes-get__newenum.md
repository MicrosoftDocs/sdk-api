---
UID: NF:tuner.IComponentTypes.get__NewEnum
title: IComponentTypes::get__NewEnum (tuner.h)
description: The get__NewEnum enumeration method supports For...Each loops in Automation clients.helpviewer_keywords: ["IComponentTypes interface [Microsoft TV Technologies]","get__NewEnum method","IComponentTypes.get__NewEnum","IComponentTypes::get__NewEnum","IComponentTypesget__NewEnum","get__NewEnum","get__NewEnum method [Microsoft TV Technologies]","get__NewEnum method [Microsoft TV Technologies]","IComponentTypes interface","mstv.icomponenttypes_get__newenum","tuner/IComponentTypes::get__NewEnum"]
old-location: mstv\icomponenttypes_get__newenum.htm
tech.root: mstv
ms.assetid: 32ff7c56-3173-4aba-9884-6e388a41192d
ms.date: 12/05/2018
ms.keywords: IComponentTypes interface [Microsoft TV Technologies],get__NewEnum method, IComponentTypes.get__NewEnum, IComponentTypes::get__NewEnum, IComponentTypesget__NewEnum, get__NewEnum, get__NewEnum method [Microsoft TV Technologies], get__NewEnum method [Microsoft TV Technologies],IComponentTypes interface, mstv.icomponenttypes_get__newenum, tuner/IComponentTypes::get__NewEnum
f1_keywords:
- tuner/IComponentTypes.get__NewEnum
dev_langs:
- c++
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
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
- tuner.h
api_name:
- IComponentTypes.get__NewEnum
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IComponentTypes::get__NewEnum


## -description



The <b>get__NewEnum</b> enumeration method supports <code>For...Each</code> loops in Automation clients.




## -parameters




### -param ppNewEnum [out]

Address of an interface pointer to an <b>IEnumVARIANT</b> object that will receive the new collection.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -remarks



This method is provided to enable scripting and Visual Basic applications to iterate through the collection in a <code>For...Each</code> loop. C++ applications should use the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-icomponenttypes-enumcomponenttypes">IComponentTypes::EnumComponentTypes</a> method.

The returned <b>IEnumVARIANT</b> interface is not thread safe, because it is intended primarily for use by Automation clients. Clients should not call methods on the interface from more than one thread.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-icomponenttypes">IComponentTypes Interface</a>
 

 

