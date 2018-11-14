---
UID: NF:pla.IDataCollectorSet.Delete
title: IDataCollectorSet::Delete
author: windows-sdk-content
description: Deletes the persisted copy of the data collector set if the set is not running.
old-location: pla\idatacollectorset_delete.htm
tech.root: PLA
ms.assetid: 35e95d41-0d6c-428a-a167-6667275d4fb7
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: Delete, Delete method [PLA], Delete method [PLA],IDataCollectorSet interface, IDataCollectorSet interface [PLA],Delete method, IDataCollectorSet.Delete, IDataCollectorSet::Delete, base.idatacollectorset_delete, pla.idatacollectorset_delete, pla/IDataCollectorSet::Delete
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: pla.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.dll: Pla.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Pla.dll
api_name:
 - IDataCollectorSet.Delete
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- pla.h
: 
- IDataCollectorSet.Delete
: 
---

# IDataCollectorSet::Delete


## -description


Deletes the persisted copy of the data collector set if the set is not running.


## -parameters






## -returns



Returns S_OK if successful. The following table shows a possible error value.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(RPC_S_SERVER_UNAVAILABLE)</b></dt>
</dl>
</td>
<td width="60%">
The RPC server is not available. The method is unable to delete the data collector set remotely. To delete the data collector set on a remote computer running  Windows Vista, enable Performance Logs and Alerts in <b>Windows Firewall Settings</b> on the remote computer.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/a4ae0874-4ee6-46a1-9811-8cd4be26859c">IDataCollectorSet</a>



<a href="https://msdn.microsoft.com/d957d34d-5455-486a-bd54-28afd7e6f979">IDataCollectorSet::Status</a>
 

 

