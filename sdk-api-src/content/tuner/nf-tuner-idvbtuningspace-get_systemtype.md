---
UID: NF:tuner.IDVBTuningSpace.get_SystemType
title: IDVBTuningSpace::get_SystemType
author: windows-sdk-content
description: The get_SystemType method retrieves the system type.
old-location: mstv\idvbtuningspace_get_systemtype.htm
old-project: mstv
ms.assetid: 4e08d142-6ae3-4da7-ba3c-59fdf07a2f10
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IDVBTuningSpace interface [Microsoft TV Technologies],get_SystemType method, IDVBTuningSpace.get_SystemType, IDVBTuningSpace::get_SystemType, IDVBTuningSpaceget_SystemType, get_SystemType, get_SystemType method [Microsoft TV Technologies], get_SystemType method [Microsoft TV Technologies],IDVBTuningSpace interface, mstv.idvbtuningspace_get_systemtype, tuner/IDVBTuningSpace::get_SystemType
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
req.typenames: BITMAP_RENDERER_STATISTICS, *PBITMAP_RENDERER_STATISTICS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	tuner.h
api_name:
-	IDVBTuningSpace.get_SystemType
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IDVBTuningSpace::get_SystemType


## -description



The <b>get_SystemType</b> method retrieves the system type.




## -parameters




### -param SysType






#### - pSysType [out]

Pointer to a variable of type <a href="https://msdn.microsoft.com/library/windows/hardware/ff558733">DVBSystemType</a> that receives the system type.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -see-also




<a href="https://msdn.microsoft.com/fba3c7f3-61f8-4704-8068-cb1d3171345a">IDVBTuningSpace Interface</a>
 

 

