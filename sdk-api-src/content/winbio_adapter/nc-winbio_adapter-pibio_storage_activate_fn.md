---
UID: NC:winbio_adapter.PIBIO_STORAGE_ACTIVATE_FN
title: PIBIO_STORAGE_ACTIVATE_FN
author: windows-sdk-content
description: Gives the Storage Adapter the chance to perform any work needed to bring the storage component out of an idle state.
old-location: secbiomet\storageadapteractivate.htm
old-project: secbiomet
ms.assetid: 2E9B5191-94F2-4954-BE3A-78803ABBAD07
ms.author: windowssdkdev
ms.date: 04/25/2018
ms.keywords: PIBIO_STORAGE_ACTIVATE_FN, PIBIO_STORAGE_ACTIVATE_FN callback, StorageAdapterActivate, StorageAdapterActivate callback function [Windows Biometric Framework API], secbiomet.storageadapteractivate, winbio_adapter/StorageAdapterActivate
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WINBIO_ASYNC_RESULT, *PWINBIO_ASYNC_RESULT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Winbio_adapter.h
api_name:
 - StorageAdapterActivate
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# PIBIO_STORAGE_ACTIVATE_FN callback function


## -description


Called by the Windows Biometric Framework to give the Storage Adapter the chance to perform any work needed to bring the storage component out of an idle state.


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

Neither the Sensor nor the Engine adapters have been activated when this method is called.

Returning any <b>HRESULT</b> other than <b>S_OK</b> will cause the Windows Biometric Framework to log the error and abort the activation of the biometric unit.

This method executes in the context of the sensor control thread that will process all other requests for the unit, including deactivation.



