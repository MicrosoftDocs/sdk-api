---
UID: NF:tuner.ITuningSpaceContainer.get__NewEnum
title: ITuningSpaceContainer::get__NewEnum (tuner.h)
description: The get__NewEnum method supports For...Each loops in Automation clients.
helpviewer_keywords: ["ITuningSpaceContainer interface [Microsoft TV Technologies]","get__NewEnum method","ITuningSpaceContainer.get__NewEnum","ITuningSpaceContainer::get__NewEnum","ITuningSpaceContainerget__NewEnum","get__NewEnum","get__NewEnum method [Microsoft TV Technologies]","get__NewEnum method [Microsoft TV Technologies]","ITuningSpaceContainer interface","mstv.ituningspacecontainer_get__newenum","tuner/ITuningSpaceContainer::get__NewEnum"]
old-location: mstv\ituningspacecontainer_get__newenum.htm
tech.root: mstv
ms.assetid: f2bcd80b-b36c-44b1-9a87-beda7ae12117
ms.date: 12/05/2018
ms.keywords: ITuningSpaceContainer interface [Microsoft TV Technologies],get__NewEnum method, ITuningSpaceContainer.get__NewEnum, ITuningSpaceContainer::get__NewEnum, ITuningSpaceContainerget__NewEnum, get__NewEnum, get__NewEnum method [Microsoft TV Technologies], get__NewEnum method [Microsoft TV Technologies],ITuningSpaceContainer interface, mstv.ituningspacecontainer_get__newenum, tuner/ITuningSpaceContainer::get__NewEnum
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
 - ITuningSpaceContainer::get__NewEnum
 - tuner/ITuningSpaceContainer::get__NewEnum
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
 - ITuningSpaceContainer.get__NewEnum
---

# ITuningSpaceContainer::get__NewEnum


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get__NewEnum</b> method supports <code>For...Each</code> loops in Automation clients.

## -parameters

### -param NewEnum [out]

Pointer to a variable that receives an <b>IEnumVARIANT</b> interface pointer. The caller must release the interface.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -remarks

This method is provided to enable scripting and Visual Basic  applications to iterate through the collection in a <code>For...Each</code> loop. C++ applications should use the <a href="/previous-versions/windows/desktop/api/tuner/nf-tuner-ituningspacecontainer-get_enumtuningspaces">ITuningSpaceContainer::get_EnumTuningSpaces</a> method.

The returned <b>IEnumVARIANT</b> interface is not thread safe, because it is intended primarily for use by Automation clients. Clients should not call methods on the interface from more than one thread.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ituningspacecontainer">ITuningSpaceContainer Interface</a>