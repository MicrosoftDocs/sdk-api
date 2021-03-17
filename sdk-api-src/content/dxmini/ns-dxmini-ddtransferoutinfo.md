---
UID: NS:dxmini._DDTRANSFEROUTINFO
title: DDTRANSFEROUTINFO (dxmini.h)
description: The DDTRANSFEROUTINFO structure returns the polarity of the field being captured.
helpviewer_keywords: ["*PDDTRANSFEROUTINFO","DDTRANSFEROUTINFO","DDTRANSFEROUTINFO structure [Display Devices]","PDDTRANSFEROUTINFO","PDDTRANSFEROUTINFO structure pointer [Display Devices]","Video_Structs_c2b03ae4-21b0-4c16-8ddc-e3ef4c79e6ff.xml","display.ddtransferoutinfo","dxmini/DDTRANSFEROUTINFO","dxmini/PDDTRANSFEROUTINFO"]
old-location: display\ddtransferoutinfo.htm
tech.root: display
ms.assetid: 0c029912-0540-438a-a255-aeb1a58ad275
ms.date: 12/05/2018
ms.keywords: '*PDDTRANSFEROUTINFO, DDTRANSFEROUTINFO, DDTRANSFEROUTINFO structure [Display Devices], PDDTRANSFEROUTINFO, PDDTRANSFEROUTINFO structure pointer [Display Devices], Video_Structs_c2b03ae4-21b0-4c16-8ddc-e3ef4c79e6ff.xml, display.ddtransferoutinfo, dxmini/DDTRANSFEROUTINFO, dxmini/PDDTRANSFEROUTINFO'
req.header: dxmini.h
req.include-header: Dxmini.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: DDTRANSFEROUTINFO, *PDDTRANSFEROUTINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DDTRANSFEROUTINFO
 - dxmini/_DDTRANSFEROUTINFO
 - PDDTRANSFEROUTINFO
 - dxmini/PDDTRANSFEROUTINFO
 - DDTRANSFEROUTINFO
 - dxmini/DDTRANSFEROUTINFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dxmini.h
api_name:
 - DDTRANSFEROUTINFO
---

# DDTRANSFEROUTINFO structure


## -description

The DDTRANSFEROUTINFO structure returns the polarity of the field being captured.

## -struct-fields

### -field dwBufferPolarity

Specifies the polarity of the field being captured. This value is set to true if the current video field is the even field of an interlaced video signal and false otherwise.

## -see-also

<a href="/windows/desktop/api/dxmini/nc-dxmini-pdx_transfer">DxTransfer</a>