---
UID: NF:comsvcs.IDispenserDriver.DestroyResource
title: IDispenserDriver::DestroyResource method
author: windows-driver-content
description: Destroys a resource.
old-location: cos\idispenserdriver_destroyresource.htm
old-project: cossdk
ms.assetid: 94e3e340-7dde-4b7f-82a9-83cd2400bde5
ms.author: windowsdriverdev
ms.date: 4/3/2018
ms.keywords: DestroyResource method [COM+], DestroyResource method [COM+], IDispenserDriver interface, DestroyResource,IDispenserDriver.DestroyResource, IDispenserDriver, IDispenserDriver interface [COM+], DestroyResource method, IDispenserDriver::DestroyResource, _dtc_IDispenserDriver_DestroyResource, comsvcs/IDispenserDriver::DestroyResource, cos.idispenserdriver_destroyresource
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: TRACKING_COLL_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	ComSvcs.h
api_name:
-	IDispenserDriver.DestroyResource
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IDispenserDriver::DestroyResource method


## -description


Destroys a resource.


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
The Resource Dispenser does not support numeric RESIDs.

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




<a href="https://msdn.microsoft.com/dba9c616-031d-48a7-b3e3-eb28b95a573a">IDispenserDriver</a>
 

 

