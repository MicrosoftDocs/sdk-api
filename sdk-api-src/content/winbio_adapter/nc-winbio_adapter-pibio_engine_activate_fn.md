---
UID: NC:winbio_adapter.PIBIO_ENGINE_ACTIVATE_FN
title: PIBIO_ENGINE_ACTIVATE_FN
author: windows-driver-content
description: Gives the Engine Adapter the chance to perform any work needed to bring the sensor component out of an idle state.
old-location: secbiomet\engineadapteractivate.htm
old-project: SecBioMet
ms.assetid: 0E98D887-A974-4B86-934E-939DEB1946DF
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: EngineAdapterActivate, EngineAdapterActivate callback function [Windows Biometric Framework API], PIBIO_ENGINE_ACTIVATE_FN, secbiomet.engineadapteractivate, winbio_adapter/EngineAdapterActivate
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
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
req.typenames: WINBIO_ASYNC_RESULT, *PWINBIO_ASYNC_RESULT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	Winbio_adapter.h
api_name:
-	EngineAdapterActivate
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# PIBIO_ENGINE_ACTIVATE_FN callback


## -description


Called by the Windows Biometric Framework to give the Engine Adapter the chance to perform any work needed to bring the sensor component out of an idle state.


## -parameters




### -param Pipeline [in, out]

Pointer to the <a href="https://msdn.microsoft.com/b5fc2b14-b0b6-4327-a42a-ecae41c3e12a">WINBIO_PIPELINE</a> structure associated with the biometric unit performing the operation.


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



This method is called when the first client session opens a handle to an inactive biometric unit.

The Storage adapter has been activated when this method is called.

Returning any <b>HRESULT</b> other than <b>S_OK</b> will cause the Windows Biometric Framework to log the error and abort the activation of the biometric unit.

This method executes in the context of the sensor control thread that will process all other requests for the unit, including deactivation.



