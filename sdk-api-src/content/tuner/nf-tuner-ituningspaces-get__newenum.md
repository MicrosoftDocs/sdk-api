---
UID: NF:tuner.ITuningSpaces.get__NewEnum
title: ITuningSpaces::get__NewEnum (tuner.h)
description: The get__NewEnum method returns an enumerator for the collection.
helpviewer_keywords: ["ITuningSpaces interface [Microsoft TV Technologies]","get__NewEnum method","ITuningSpaces.get__NewEnum","ITuningSpaces::get__NewEnum","ITuningSpacesget__NewEnum","get__NewEnum","get__NewEnum method [Microsoft TV Technologies]","get__NewEnum method [Microsoft TV Technologies]","ITuningSpaces interface","mstv.ituningspaces_get__newenum","tuner/ITuningSpaces::get__NewEnum"]
old-location: mstv\ituningspaces_get__newenum.htm
tech.root: mstv
ms.assetid: 9f0aec7a-954d-4399-8d15-5869c5353677
ms.date: 12/05/2018
ms.keywords: ITuningSpaces interface [Microsoft TV Technologies],get__NewEnum method, ITuningSpaces.get__NewEnum, ITuningSpaces::get__NewEnum, ITuningSpacesget__NewEnum, get__NewEnum, get__NewEnum method [Microsoft TV Technologies], get__NewEnum method [Microsoft TV Technologies],ITuningSpaces interface, mstv.ituningspaces_get__newenum, tuner/ITuningSpaces::get__NewEnum
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
 - ITuningSpaces::get__NewEnum
 - tuner/ITuningSpaces::get__NewEnum
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
 - ITuningSpaces.get__NewEnum
---

# ITuningSpaces::get__NewEnum


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get__NewEnum</b> method returns an enumerator for the collection.



This method is provided to enable scripting and Visual Basic applications to iterate through the collection in a <code>For...Each</code> loop. C++ applications should use the <a href="/previous-versions/windows/desktop/api/tuner/nf-tuner-ituningspaces-get_enumtuningspaces">ITuningSpaces::get_EnumTuningSpaces</a> method.

## -parameters

### -param NewEnum [out]

Pointer to a variable that receives an <b>IEnumVARIANT</b> interface pointer. The caller must release the interface.

## -returns

Returns S_OK if successful.

## -remarks

The returned <b>IEnumVARIANT</b> interface is not thread safe, because it is intended primarily for use by Automation clients. Clients should not call methods on the interface from more than one thread.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ituningspaces">ITuningSpaces Interface</a>