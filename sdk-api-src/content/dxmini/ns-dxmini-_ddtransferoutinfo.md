---
UID: NS:dxmini._DDTRANSFEROUTINFO
title: "_DDTRANSFEROUTINFO"
author: windows-sdk-content
description: The DDTRANSFEROUTINFO structure returns the polarity of the field being captured.
old-location: display\ddtransferoutinfo.htm
tech.root: Display
ms.assetid: 0c029912-0540-438a-a255-aeb1a58ad275
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*PDDTRANSFEROUTINFO, DDTRANSFEROUTINFO, DDTRANSFEROUTINFO structure [Display Devices], PDDTRANSFEROUTINFO, PDDTRANSFEROUTINFO structure pointer [Display Devices], Video_Structs_c2b03ae4-21b0-4c16-8ddc-e3ef4c79e6ff.xml, _DDTRANSFEROUTINFO, display.ddtransferoutinfo, dxmini/DDTRANSFEROUTINFO, dxmini/PDDTRANSFEROUTINFO"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dxmini.h
api_name:
 - DDTRANSFEROUTINFO
product: Windows
targetos: Windows
req.typenames: DDTRANSFEROUTINFO, *PDDTRANSFEROUTINFO
req.redist: 
---

# _DDTRANSFEROUTINFO structure


## -description


The DDTRANSFEROUTINFO structure returns the polarity of the field being captured.


## -struct-fields




### -field dwBufferPolarity

Specifies the polarity of the field being captured. This value is set to true if the current video field is the even field of an interlaced video signal and false otherwise.


## -see-also




<a href="https://msdn.microsoft.com/62e1a5f6-9777-4acf-a531-b3554eaf89a6">DxTransfer</a>
 

 

