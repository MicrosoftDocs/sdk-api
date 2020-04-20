---
UID: NC:winbio_adapter.PIBIO_ENGINE_DEACTIVATE_FN
title: PIBIO_ENGINE_DEACTIVATE_FN (winbio_adapter.h)
description: Gives the Engine Adapter the chance to perform any work needed to put the sensor component into an idle state.helpviewer_keywords: ["EngineAdapterDeactivate","EngineAdapterDeactivate callback function [Windows Biometric Framework API]","PIBIO_ENGINE_DEACTIVATE_FN","PIBIO_ENGINE_DEACTIVATE_FN callback","secbiomet.engineadapterdeactivate","winbio_adapter/EngineAdapterDeactivate"]
old-location: secbiomet\engineadapterdeactivate.htm
tech.root: SecBioMet
ms.assetid: A7FDB75C-146C-47E9-AB3B-8457EA3304BF
ms.date: 12/05/2018
ms.keywords: EngineAdapterDeactivate, EngineAdapterDeactivate callback function [Windows Biometric Framework API], PIBIO_ENGINE_DEACTIVATE_FN, PIBIO_ENGINE_DEACTIVATE_FN callback, secbiomet.engineadapterdeactivate, winbio_adapter/EngineAdapterDeactivate
f1_keywords:
- winbio_adapter/EngineAdapterDeactivate
dev_langs:
- c++
req.header: winbio_adapter.h
req.include-header: Winbio_adapter.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
- UserDefined
api_location:
- Winbio_adapter.h
api_name:
- EngineAdapterDeactivate
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PIBIO_ENGINE_DEACTIVATE_FN callback function


## -description


Called by the Windows Biometric Framework to give the Engine Adapter the chance to perform any work needed to put the sensor component into an idle state.


## -parameters




### -param Pipeline [in, out]

Pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/winbio_adapter/ns-winbio_adapter-winbio_pipeline">WINBIO_PIPELINE</a> structure associated with the biometric unit performing the operation.


## -returns



If the function succeeds, it returns <b>S_OK</b>. If the function fails, it must return one of the following <b>HRESULT</b> values to indicate the error.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>Pipeline</i> parameter cannot be <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



This method is called when the last client using this biometric unit has closed its session handle.

This method executes in the context of the same thread that activated the biometric unit and that processed all other requests for the unit.

When this routine is called, the Storage adapter is still available.



