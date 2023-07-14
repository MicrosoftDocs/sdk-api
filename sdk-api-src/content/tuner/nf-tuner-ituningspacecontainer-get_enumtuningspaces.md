---
UID: NF:tuner.ITuningSpaceContainer.get_EnumTuningSpaces
title: ITuningSpaceContainer::get_EnumTuningSpaces (tuner.h)
description: The get_EnumTuningSpaces method retrieves a collection of all tuning spaces available on the local system.
helpviewer_keywords: ["ITuningSpaceContainer interface [Microsoft TV Technologies]","get_EnumTuningSpaces method","ITuningSpaceContainer.get_EnumTuningSpaces","ITuningSpaceContainer::get_EnumTuningSpaces","ITuningSpaceContainerget_EnumTuningSpaces","get_EnumTuningSpaces","get_EnumTuningSpaces method [Microsoft TV Technologies]","get_EnumTuningSpaces method [Microsoft TV Technologies]","ITuningSpaceContainer interface","mstv.ituningspacecontainer_get_enumtuningspaces","tuner/ITuningSpaceContainer::get_EnumTuningSpaces"]
old-location: mstv\ituningspacecontainer_get_enumtuningspaces.htm
tech.root: mstv
ms.assetid: 7cd6a691-8c47-4c26-8afd-57f6965246ff
ms.date: 12/05/2018
ms.keywords: ITuningSpaceContainer interface [Microsoft TV Technologies],get_EnumTuningSpaces method, ITuningSpaceContainer.get_EnumTuningSpaces, ITuningSpaceContainer::get_EnumTuningSpaces, ITuningSpaceContainerget_EnumTuningSpaces, get_EnumTuningSpaces, get_EnumTuningSpaces method [Microsoft TV Technologies], get_EnumTuningSpaces method [Microsoft TV Technologies],ITuningSpaceContainer interface, mstv.ituningspacecontainer_get_enumtuningspaces, tuner/ITuningSpaceContainer::get_EnumTuningSpaces
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
 - ITuningSpaceContainer::get_EnumTuningSpaces
 - tuner/ITuningSpaceContainer::get_EnumTuningSpaces
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
 - ITuningSpaceContainer.get_EnumTuningSpaces
---

# ITuningSpaceContainer::get_EnumTuningSpaces


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_EnumTuningSpaces</b> method retrieves a collection of all tuning spaces available on the local system.

## -parameters

### -param ppEnum [out]

Pointer to a variable that receives an <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ienumtuningspaces">IEnumTuningSpaces</a> interface pointer. Use this interface to enumerate the collection. The caller must release the interface.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -remarks

C++ applications use this method to get the initial list of tuning spaces defined on the local system.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ituningspacecontainer">ITuningSpaceContainer Interface</a>