---
UID: NF:comsvcs.IDispenserDriver.ResetResource
title: IDispenserDriver::ResetResource
author: windows-driver-content
description: Prepares the resource to be put back into general or enlisted inventory.
old-location: cos\idispenserdriver_resetresource.htm
old-project: cossdk
ms.assetid: 59df0703-90ea-480c-8608-7d43039b48ba
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: IDispenserDriver interface [COM+],ResetResource method, IDispenserDriver.ResetResource, IDispenserDriver::ResetResource, ResetResource, ResetResource method [COM+], ResetResource method [COM+],IDispenserDriver interface, _dtc_IDispenserDriver_ResetResource, comsvcs/IDispenserDriver::ResetResource, cos.idispenserdriver_resetresource
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
-	IDispenserDriver.ResetResource
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IDispenserDriver::ResetResource


## -description


Prepares the resource to be put back into general or enlisted inventory.


## -parameters




### -param ResId [in]

The resource to be reset.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>ResId</i> is not a valid resource handle.

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
 




## -remarks



The resource may still be enlisted at this time, so <b>ResetResource</b> cannot disrupt the enlistment.




## -see-also




<a href="https://msdn.microsoft.com/dba9c616-031d-48a7-b3e3-eb28b95a573a">IDispenserDriver</a>
 

 

