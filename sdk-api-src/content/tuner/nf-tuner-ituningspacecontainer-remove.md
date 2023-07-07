---
UID: NF:tuner.ITuningSpaceContainer.Remove
title: ITuningSpaceContainer::Remove (tuner.h)
description: The Remove method permanently removes a tuning space from the system.
helpviewer_keywords: ["ITuningSpaceContainer interface [Microsoft TV Technologies]","Remove method","ITuningSpaceContainer.Remove","ITuningSpaceContainer::Remove","ITuningSpaceContainerRemove","Remove","Remove method [Microsoft TV Technologies]","Remove method [Microsoft TV Technologies]","ITuningSpaceContainer interface","mstv.ituningspacecontainer_remove","tuner/ITuningSpaceContainer::Remove"]
old-location: mstv\ituningspacecontainer_remove.htm
tech.root: mstv
ms.assetid: 72ead181-6c5a-49d1-a789-3ae4128417c6
ms.date: 12/05/2018
ms.keywords: ITuningSpaceContainer interface [Microsoft TV Technologies],Remove method, ITuningSpaceContainer.Remove, ITuningSpaceContainer::Remove, ITuningSpaceContainerRemove, Remove, Remove method [Microsoft TV Technologies], Remove method [Microsoft TV Technologies],ITuningSpaceContainer interface, mstv.ituningspacecontainer_remove, tuner/ITuningSpaceContainer::Remove
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
 - ITuningSpaceContainer::Remove
 - tuner/ITuningSpaceContainer::Remove
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
 - ITuningSpaceContainer.Remove
---

# ITuningSpaceContainer::Remove


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>Remove</b> method permanently removes a tuning space from the system.

## -parameters

### -param Index [in]

Variable of type <b>VARIANT</b> that specifies the ID of the tuning space to remove.

## -returns

Returns S_OK if successful. If the specified tuning space was invalid or corrupted in the Registry, this method will delete whatever information is there and return S_FALSE.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ituningspacecontainer">ITuningSpaceContainer Interface</a>