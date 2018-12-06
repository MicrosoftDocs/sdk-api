---
UID: NC:winbio_adapter.PIBIO_STORAGE_DEACTIVATE_FN
title: PIBIO_STORAGE_DEACTIVATE_FN
author: windows-sdk-content
description: Gives the Storage Adapter the chance to perform any work needed to put the storage component into an idle state.
old-location: secbiomet\storageadapterdeactivate.htm
tech.root: SecBioMet
ms.assetid: 95AAEE98-2DA6-4A2C-BF0C-DBE193346FE1
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: PIBIO_STORAGE_DEACTIVATE_FN, PIBIO_STORAGE_DEACTIVATE_FN callback, StorageAdapterDeactivate, StorageAdapterDeactivate callback function [Windows Biometric Framework API], secbiomet.storageadapterdeactivate, winbio_adapter/StorageAdapterDeactivate
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
 - StorageAdapterDeactivate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PIBIO_STORAGE_DEACTIVATE_FN callback function


## -description


Called by the Windows Biometric Framework to give the Storage Adapter the chance to perform any work needed to put the storage component into an idle state.


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



This method is called when the last client using this biometric unit has closed its session handle.

This method executes in the context of the same thread that activated the biometric unit and that processed all other requests for the unit.



