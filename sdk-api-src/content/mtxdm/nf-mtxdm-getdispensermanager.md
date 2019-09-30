---
UID: NF:mtxdm.GetDispenserManager
title: GetDispenserManager function (mtxdm.h)
author: windows-sdk-content
description: Retrieves the dispenser manager's IDispenserManager interface.
old-location: cos\getdispensermanager.htm
tech.root: cossdk
ms.assetid: db344236-a8be-49ec-91fd-dfcc0bd4412c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetDispenserManager, GetDispenserManager function [COM+], _dtc_GetDispenserManager_Function, cos.getdispensermanager, mtxdm/GetDispenserManager
ms.topic: function
f1_keywords: 
 - "mtxdm/GetDispenserManager"
req.header: mtxdm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: MtxDM.lib
req.dll: MtxDM.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - MtxDM.dll
api_name:
 - GetDispenserManager
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetDispenserManager function


## -description


Retrieves the dispenser manager's <a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-idispensermanager">IDispenserManager</a> interface.


## -parameters




### -param Arg1 [out]

A pointer to the location that receives the <a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-idispensermanager">IDispenserManager</a> interface pointer.


## -returns



If the method succeeds, the return value is S_OK. Otherwise, it is E_FAIL.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-idispensermanager">IDispenserManager</a>
 

 

