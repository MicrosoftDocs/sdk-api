---
UID: NF:tuner.ITuningSpaceContainer.get_Count
title: ITuningSpaceContainer::get_Count (tuner.h)
description: The get_Count method retrieves the number of tuning spaces currently available on the local system.
helpviewer_keywords: ["ITuningSpaceContainer interface [Microsoft TV Technologies]","get_Count method","ITuningSpaceContainer.get_Count","ITuningSpaceContainer::get_Count","ITuningSpaceContainerget_Count","get_Count","get_Count method [Microsoft TV Technologies]","get_Count method [Microsoft TV Technologies]","ITuningSpaceContainer interface","mstv.ituningspacecontainer_get_count","tuner/ITuningSpaceContainer::get_Count"]
old-location: mstv\ituningspacecontainer_get_count.htm
tech.root: mstv
ms.assetid: 9dfa7700-fef5-4e97-855b-0670cc380af0
ms.date: 12/05/2018
ms.keywords: ITuningSpaceContainer interface [Microsoft TV Technologies],get_Count method, ITuningSpaceContainer.get_Count, ITuningSpaceContainer::get_Count, ITuningSpaceContainerget_Count, get_Count, get_Count method [Microsoft TV Technologies], get_Count method [Microsoft TV Technologies],ITuningSpaceContainer interface, mstv.ituningspacecontainer_get_count, tuner/ITuningSpaceContainer::get_Count
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
 - ITuningSpaceContainer::get_Count
 - tuner/ITuningSpaceContainer::get_Count
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
 - ITuningSpaceContainer.get_Count
---

# ITuningSpaceContainer::get_Count


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_Count</b> method retrieves the number of tuning spaces currently available on the local system.

## -parameters

### -param Count [out]

Pointer to a variable receives the number of tuning spaces.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ituningspacecontainer">ITuningSpaceContainer Interface</a>