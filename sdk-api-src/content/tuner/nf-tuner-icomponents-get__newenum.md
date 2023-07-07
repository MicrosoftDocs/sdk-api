---
UID: NF:tuner.IComponents.get__NewEnum
title: IComponents::get__NewEnum (tuner.h)
description: The get__NewEnum enumeration method supports For...Each loops in Automation clients.
helpviewer_keywords: ["IComponents interface [Microsoft TV Technologies]","get__NewEnum method","IComponents.get__NewEnum","IComponents::get__NewEnum","IComponentsget__NewEnum","get__NewEnum","get__NewEnum method [Microsoft TV Technologies]","get__NewEnum method [Microsoft TV Technologies]","IComponents interface","mstv.icomponents_get__newenum","tuner/IComponents::get__NewEnum"]
old-location: mstv\icomponents_get__newenum.htm
tech.root: mstv
ms.assetid: fcb965f4-8fd6-415f-8fb6-a80d0c92731d
ms.date: 12/05/2018
ms.keywords: IComponents interface [Microsoft TV Technologies],get__NewEnum method, IComponents.get__NewEnum, IComponents::get__NewEnum, IComponentsget__NewEnum, get__NewEnum, get__NewEnum method [Microsoft TV Technologies], get__NewEnum method [Microsoft TV Technologies],IComponents interface, mstv.icomponents_get__newenum, tuner/IComponents::get__NewEnum
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IComponents::get__NewEnum
 - tuner/IComponents::get__NewEnum
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tuner.h
api_name:
 - IComponents.get__NewEnum
---

# IComponents::get__NewEnum


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get__NewEnum</b> enumeration method supports <code>For...Each</code> loops in Automation clients.

## -parameters

### -param ppNewEnum [out]

Address of an <b>IEnumVARIANT</b> interface pointer that will receive the enumeration.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -remarks

This method is provided so that scripting and Visual Basic applications can iterate through the collection in a <code>For...Each</code> loop. C++ applications should use the <a href="/previous-versions/windows/desktop/api/tuner/nf-tuner-icomponents-enumcomponents">IComponents::EnumComponents</a> method.

The returned <b>IEnumVARIANT</b> interface is not thread safe, because it is intended primarily for use by Automation clients. Clients should not call methods on the interface from more than one thread.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-icomponents">IComponents Interface</a>