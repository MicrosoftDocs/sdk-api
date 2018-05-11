---
UID: NF:tuner.IRegisterTuner.Register
title: IRegisterTuner::Register
author: windows-driver-content
description: This feature is expected to be available on a future version of the Windows operating system.
old-location: mstv\iregistertuner_register.htm
old-project: mstv
ms.assetid: 17a59666-1915-496f-9474-ddd6b3da58f5
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: IRegisterTuner interface [Microsoft TV Technologies],Register method, IRegisterTuner.Register, IRegisterTuner::Register, IRegisterTunerRegister, Register, Register method [Microsoft TV Technologies], Register method [Microsoft TV Technologies],IRegisterTuner interface, mstv.iregistertuner_register, tuner/IRegisterTuner::Register
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
-	IRegisterTuner.Register
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IRegisterTuner::Register


## -description



This feature is expected to be available on a future version of the Windows operating system.
        



The <b>Register</b> method registers an apartment-threaded tuner with the tuner marshaller and registers the tuner marshaller with the graph service provider.


## -parameters




### -param pTuner [in]

Pointer to a variable that specifies the tuner.


### -param pGraph [in]

Pointer to a variable that specifies the graph filter provider.


## -returns



When the method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/99e88361-f5d3-43b7-b879-2e1c44859af4">IRegisterTuner Interface</a>
 

 

