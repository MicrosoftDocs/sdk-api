---
UID: NF:mtxdm.GetDispenserManager
title: GetDispenserManager function (mtxdm.h)
description: Retrieves the dispenser manager's IDispenserManager interface.
helpviewer_keywords: ["GetDispenserManager","GetDispenserManager function [COM+]","_dtc_GetDispenserManager_Function","cos.getdispensermanager","mtxdm/GetDispenserManager"]
old-location: cos\getdispensermanager.htm
tech.root: cos
ms.assetid: db344236-a8be-49ec-91fd-dfcc0bd4412c
ms.date: 12/05/2018
ms.keywords: GetDispenserManager, GetDispenserManager function [COM+], _dtc_GetDispenserManager_Function, cos.getdispensermanager, mtxdm/GetDispenserManager
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetDispenserManager
 - mtxdm/GetDispenserManager
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - MtxDM.dll
api_name:
 - GetDispenserManager
---

# GetDispenserManager function


## -description

Retrieves the dispenser manager's <a href="/windows/desktop/api/comsvcs/nn-comsvcs-idispensermanager">IDispenserManager</a> interface.

## -parameters

### -param unnamedParam1 [out]

A pointer to the location that receives the <a href="/windows/desktop/api/comsvcs/nn-comsvcs-idispensermanager">IDispenserManager</a> interface pointer.

## -returns

If the method succeeds, the return value is S_OK. Otherwise, it is E_FAIL.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-idispensermanager">IDispenserManager</a>