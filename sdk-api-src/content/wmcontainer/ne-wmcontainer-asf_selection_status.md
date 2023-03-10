---
UID: NE:wmcontainer.ASF_SELECTION_STATUS
title: ASF_SELECTION_STATUS (wmcontainer.h)
description: Defines the selection options for an ASF stream.
helpviewer_keywords: ["1571650b-4d5c-49ae-9e6d-77ef4ae7ae59","ASF_SELECTION_STATUS","ASF_SELECTION_STATUS enumeration [Media Foundation]","ASF_STATUS_ALLDATAUNITS","ASF_STATUS_CLEANPOINTSONLY","ASF_STATUS_NOTSELECTED","mf.asf_selection_status","wmcontainer/ASF_SELECTION_STATUS","wmcontainer/ASF_STATUS_ALLDATAUNITS","wmcontainer/ASF_STATUS_CLEANPOINTSONLY","wmcontainer/ASF_STATUS_NOTSELECTED"]
old-location: mf\asf_selection_status.htm
tech.root: mf
ms.assetid: 1571650b-4d5c-49ae-9e6d-77ef4ae7ae59
ms.date: 12/05/2018
ms.keywords: 1571650b-4d5c-49ae-9e6d-77ef4ae7ae59, ASF_SELECTION_STATUS, ASF_SELECTION_STATUS enumeration [Media Foundation], ASF_STATUS_ALLDATAUNITS, ASF_STATUS_CLEANPOINTSONLY, ASF_STATUS_NOTSELECTED, mf.asf_selection_status, wmcontainer/ASF_SELECTION_STATUS, wmcontainer/ASF_STATUS_ALLDATAUNITS, wmcontainer/ASF_STATUS_CLEANPOINTSONLY, wmcontainer/ASF_STATUS_NOTSELECTED
req.header: wmcontainer.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: ASF_SELECTION_STATUS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ASF_SELECTION_STATUS
 - wmcontainer/ASF_SELECTION_STATUS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wmcontainer.h
api_name:
 - ASF_SELECTION_STATUS
---

# ASF_SELECTION_STATUS enumeration


## -description

Defines the selection options for an ASF stream.

## -enum-fields

### -field ASF_STATUS_NOTSELECTED:0

No samples from the stream are delivered.

### -field ASF_STATUS_CLEANPOINTSONLY:1

Only samples from the stream that are clean points are delivered.

### -field ASF_STATUS_ALLDATAUNITS:2

All samples from the stream are delivered.

## -see-also

<a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamselector-getbandwidthstep">IMFASFStreamSelector::GetBandwidthStep</a>



<a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamselector-getoutputoverride">IMFASFStreamSelector::GetOutputOverride</a>



<a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamselector-setoutputoverride">IMFASFStreamSelector::SetOutputOverride</a>



<a href="/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>
