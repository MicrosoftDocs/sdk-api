---
UID: NF:tuner.ITuningSpaceContainer.put_MaxCount
title: ITuningSpaceContainer::put_MaxCount (tuner.h)
description: The put_MaxCount method sets the maximum number of tuning spaces allowed on the system.
helpviewer_keywords: ["ITuningSpaceContainer interface [Microsoft TV Technologies]","put_MaxCount method","ITuningSpaceContainer.put_MaxCount","ITuningSpaceContainer::put_MaxCount","ITuningSpaceContainerput_MaxCount","mstv.ituningspacecontainer_put_maxcount","put_MaxCount","put_MaxCount method [Microsoft TV Technologies]","put_MaxCount method [Microsoft TV Technologies]","ITuningSpaceContainer interface","tuner/ITuningSpaceContainer::put_MaxCount"]
old-location: mstv\ituningspacecontainer_put_maxcount.htm
tech.root: mstv
ms.assetid: a469557b-c01a-4922-99ad-641c74130cc9
ms.date: 12/05/2018
ms.keywords: ITuningSpaceContainer interface [Microsoft TV Technologies],put_MaxCount method, ITuningSpaceContainer.put_MaxCount, ITuningSpaceContainer::put_MaxCount, ITuningSpaceContainerput_MaxCount, mstv.ituningspacecontainer_put_maxcount, put_MaxCount, put_MaxCount method [Microsoft TV Technologies], put_MaxCount method [Microsoft TV Technologies],ITuningSpaceContainer interface, tuner/ITuningSpaceContainer::put_MaxCount
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
 - ITuningSpaceContainer::put_MaxCount
 - tuner/ITuningSpaceContainer::put_MaxCount
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
 - ITuningSpaceContainer.put_MaxCount
---

# ITuningSpaceContainer::put_MaxCount


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_MaxCount</b> method sets the maximum number of tuning spaces allowed on the system.

## -parameters

### -param MaxCount [in]

Specifies the maximum number of tuning spaces.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ituningspacecontainer">ITuningSpaceContainer Interface</a>