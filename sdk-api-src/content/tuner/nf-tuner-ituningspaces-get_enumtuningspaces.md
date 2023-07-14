---
UID: NF:tuner.ITuningSpaces.get_EnumTuningSpaces
title: ITuningSpaces::get_EnumTuningSpaces (tuner.h)
description: The get_EnumTuningSpaces method returns an enumerator for the collection.
helpviewer_keywords: ["ITuningSpaces interface [Microsoft TV Technologies]","get_EnumTuningSpaces method","ITuningSpaces.get_EnumTuningSpaces","ITuningSpaces::get_EnumTuningSpaces","ITuningSpacesget_EnumTuningSpaces","get_EnumTuningSpaces","get_EnumTuningSpaces method [Microsoft TV Technologies]","get_EnumTuningSpaces method [Microsoft TV Technologies]","ITuningSpaces interface","mstv.ituningspaces_get_enumtuningspaces","tuner/ITuningSpaces::get_EnumTuningSpaces"]
old-location: mstv\ituningspaces_get_enumtuningspaces.htm
tech.root: mstv
ms.assetid: 0d3fb395-191c-4862-8eba-07b5502dc5d4
ms.date: 12/05/2018
ms.keywords: ITuningSpaces interface [Microsoft TV Technologies],get_EnumTuningSpaces method, ITuningSpaces.get_EnumTuningSpaces, ITuningSpaces::get_EnumTuningSpaces, ITuningSpacesget_EnumTuningSpaces, get_EnumTuningSpaces, get_EnumTuningSpaces method [Microsoft TV Technologies], get_EnumTuningSpaces method [Microsoft TV Technologies],ITuningSpaces interface, mstv.ituningspaces_get_enumtuningspaces, tuner/ITuningSpaces::get_EnumTuningSpaces
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
 - ITuningSpaces::get_EnumTuningSpaces
 - tuner/ITuningSpaces::get_EnumTuningSpaces
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
 - ITuningSpaces.get_EnumTuningSpaces
---

# ITuningSpaces::get_EnumTuningSpaces


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_EnumTuningSpaces</b> method returns an enumerator for the collection.

## -parameters

### -param NewEnum [out]

Pointer to a variable that receives an <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ienumtuningspaces">IEnumTuningSpaces</a> interface pointer. Use this interface to iterate through the collection. The caller must release the interface.

## -returns

Returns S_OK if successful.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ituningspaces">ITuningSpaces Interface</a>