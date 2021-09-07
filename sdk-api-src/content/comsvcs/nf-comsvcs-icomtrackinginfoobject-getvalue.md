---
UID: NF:comsvcs.IComTrackingInfoObject.GetValue
title: IComTrackingInfoObject::GetValue (comsvcs.h)
description: Retrieves the value of the specified property.
helpviewer_keywords: ["GetValue","GetValue method [COM+]","GetValue method [COM+]","IComTrackingInfoObject interface","IComTrackingInfoObject interface [COM+]","GetValue method","IComTrackingInfoObject.GetValue","IComTrackingInfoObject::GetValue","_dtc_IComTrackingInfoObject_GetValue","comsvcs/IComTrackingInfoObject::GetValue","cos.icomtrackinginfoobject_getvalue"]
old-location: cos\icomtrackinginfoobject_getvalue.htm
tech.root: cos
ms.assetid: 38f5fc3d-eecd-42e5-92ea-df2b096aa1cc
ms.date: 12/05/2018
ms.keywords: GetValue, GetValue method [COM+], GetValue method [COM+],IComTrackingInfoObject interface, IComTrackingInfoObject interface [COM+],GetValue method, IComTrackingInfoObject.GetValue, IComTrackingInfoObject::GetValue, _dtc_IComTrackingInfoObject_GetValue, comsvcs/IComTrackingInfoObject::GetValue, cos.icomtrackinginfoobject_getvalue
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
 - IComTrackingInfoObject::GetValue
 - comsvcs/IComTrackingInfoObject::GetValue
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
 - IComTrackingInfoObject.GetValue
---

# IComTrackingInfoObject::GetValue


## -description

Retrieves the value of the specified property.

## -parameters

### -param szPropertyName [in]

The name of the property.

### -param pvarOut [out]

The value of the property.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icomtrackinginfoobject">IComTrackingInfoObject</a>