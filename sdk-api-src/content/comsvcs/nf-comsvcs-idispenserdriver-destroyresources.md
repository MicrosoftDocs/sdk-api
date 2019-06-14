---
UID: NF:comsvcs.IDispenserDriver.DestroyResourceS
title: IDispenserDriver::DestroyResourceS (comsvcs.h)
author: windows-sdk-content
description: Destroys a resource (string resource version).
old-location: cos\idispenserdriver_destroyresources.htm
tech.root: cossdk
ms.assetid: 0c7fe9ca-8a27-4459-a95d-084d717d3a65
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DestroyResourceS, DestroyResourceS method [COM+], DestroyResourceS method [COM+],IDispenserDriver interface, IDispenserDriver interface [COM+],DestroyResourceS method, IDispenserDriver.DestroyResourceS, IDispenserDriver::DestroyResourceS, _dtc_IDispenserDriver_DestroyResourceS, comsvcs/IDispenserDriver::DestroyResourceS, cos.idispenserdriver_destroyresources
ms.topic: method
req.header: comsvcs.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IDispenserDriver.DestroyResourceS
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDispenserDriver::DestroyResourceS


## -description


Destroys a resource (string resource version).


## -parameters




### -param ResId [in]

The resource that the Dispenser Manager is asking the Resource Dispenser to destroy.


## -returns



This method can return the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The Resource Dispenser does not support numeric SRESIDs.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The method failed.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-idispenserdriver">IDispenserDriver</a>
 

 

