---
UID: NF:comsvcs.IComTrackingInfoEvents.OnNewTrackingInfo
title: IComTrackingInfoEvents::OnNewTrackingInfo (comsvcs.h)
description: Generated when the tracking information for a collection changes.
helpviewer_keywords: ["IComTrackingInfoEvents interface [COM+]","OnNewTrackingInfo method","IComTrackingInfoEvents.OnNewTrackingInfo","IComTrackingInfoEvents::OnNewTrackingInfo","OnNewTrackingInfo","OnNewTrackingInfo method [COM+]","OnNewTrackingInfo method [COM+]","IComTrackingInfoEvents interface","_dtc_IComTrackingInfoEvents_OnNewTrackingInfo","comsvcs/IComTrackingInfoEvents::OnNewTrackingInfo","cos.icomtrackinginfoevents_onnewtrackinginfo"]
old-location: cos\icomtrackinginfoevents_onnewtrackinginfo.htm
tech.root: cos
ms.assetid: a63f6782-b50a-4457-bd51-4eba8c413a47
ms.date: 12/05/2018
ms.keywords: IComTrackingInfoEvents interface [COM+],OnNewTrackingInfo method, IComTrackingInfoEvents.OnNewTrackingInfo, IComTrackingInfoEvents::OnNewTrackingInfo, OnNewTrackingInfo, OnNewTrackingInfo method [COM+], OnNewTrackingInfo method [COM+],IComTrackingInfoEvents interface, _dtc_IComTrackingInfoEvents_OnNewTrackingInfo, comsvcs/IComTrackingInfoEvents::OnNewTrackingInfo, cos.icomtrackinginfoevents_onnewtrackinginfo
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IComTrackingInfoEvents::OnNewTrackingInfo
 - comsvcs/IComTrackingInfoEvents::OnNewTrackingInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IComTrackingInfoEvents.OnNewTrackingInfo
---

# IComTrackingInfoEvents::OnNewTrackingInfo


## -description

Generated when the tracking information for a collection changes.

## -parameters

### -param pToplevelCollection [in]

A pointer to the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface of the collection for which the tracking information has changed.

## -returns

The user verifies the return values from this method.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icomtrackinginfoevents">IComTrackingInfoEvents</a>