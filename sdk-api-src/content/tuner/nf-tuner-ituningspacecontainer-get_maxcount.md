---
UID: NF:tuner.ITuningSpaceContainer.get_MaxCount
title: ITuningSpaceContainer::get_MaxCount (tuner.h)
description: The get_MaxCount method retrieves the maximum number of tuning spaces allowed on the system.
helpviewer_keywords: ["ITuningSpaceContainer interface [Microsoft TV Technologies]","get_MaxCount method","ITuningSpaceContainer.get_MaxCount","ITuningSpaceContainer::get_MaxCount","ITuningSpaceContainerget_MaxCount","get_MaxCount","get_MaxCount method [Microsoft TV Technologies]","get_MaxCount method [Microsoft TV Technologies]","ITuningSpaceContainer interface","mstv.ituningspacecontainer_get_maxcount","tuner/ITuningSpaceContainer::get_MaxCount"]
old-location: mstv\ituningspacecontainer_get_maxcount.htm
tech.root: mstv
ms.assetid: 72692bc6-a210-4e60-9c04-14a7ea531cb4
ms.date: 12/05/2018
ms.keywords: ITuningSpaceContainer interface [Microsoft TV Technologies],get_MaxCount method, ITuningSpaceContainer.get_MaxCount, ITuningSpaceContainer::get_MaxCount, ITuningSpaceContainerget_MaxCount, get_MaxCount, get_MaxCount method [Microsoft TV Technologies], get_MaxCount method [Microsoft TV Technologies],ITuningSpaceContainer interface, mstv.ituningspacecontainer_get_maxcount, tuner/ITuningSpaceContainer::get_MaxCount
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
 - ITuningSpaceContainer::get_MaxCount
 - tuner/ITuningSpaceContainer::get_MaxCount
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
 - ITuningSpaceContainer.get_MaxCount
---

# ITuningSpaceContainer::get_MaxCount


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_MaxCount</b> method retrieves the maximum number of tuning spaces allowed on the system.

## -parameters

### -param MaxCount [out]

Pointer to a variable that receives the maximum number of tuning spaces.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ituningspacecontainer">ITuningSpaceContainer Interface</a>