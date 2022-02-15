---
UID: NF:mfidl.IMFVideoProcessorControl.SetConstrictionSize
title: IMFVideoProcessorControl::SetConstrictionSize (mfidl.h)
description: Specifies the amount of downsampling to perform on the output.
helpviewer_keywords: ["IMFVideoProcessorControl interface [Media Foundation]","SetConstrictionSize method","IMFVideoProcessorControl.SetConstrictionSize","IMFVideoProcessorControl::SetConstrictionSize","SetConstrictionSize","SetConstrictionSize method [Media Foundation]","SetConstrictionSize method [Media Foundation]","IMFVideoProcessorControl interface","mf.imfvideoprocessorcontrol_setconstrictionsize","mfidl/IMFVideoProcessorControl::SetConstrictionSize"]
old-location: mf\imfvideoprocessorcontrol_setconstrictionsize.htm
tech.root: mf
ms.assetid: 876F8BA0-9F05-48C6-ADE9-D65E7682C545
ms.date: 12/05/2018
ms.keywords: IMFVideoProcessorControl interface [Media Foundation],SetConstrictionSize method, IMFVideoProcessorControl.SetConstrictionSize, IMFVideoProcessorControl::SetConstrictionSize, SetConstrictionSize, SetConstrictionSize method [Media Foundation], SetConstrictionSize method [Media Foundation],IMFVideoProcessorControl interface, mf.imfvideoprocessorcontrol_setconstrictionsize, mfidl/IMFVideoProcessorControl::SetConstrictionSize
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - IMFVideoProcessorControl::SetConstrictionSize
 - mfidl/IMFVideoProcessorControl::SetConstrictionSize
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfidl.h
api_name:
 - IMFVideoProcessorControl.SetConstrictionSize
---

# IMFVideoProcessorControl::SetConstrictionSize


## -description

Specifies the amount of downsampling to perform on the output.

## -parameters

### -param pConstrictionSize [in]

The sampling size.

To disable constriction, set this parameter to <b>NULL</b>.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfvideoprocessorcontrol">IMFVideoProcessorControl</a>