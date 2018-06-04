---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IEmptyVolumeCache::GetSpaceUsed


## -description


Requests the amount of disk space that the disk cleanup handler can free.


## -parameters




### -param pdwlSpaceUsed




### -param picb [in]

Type: <b>IEmptyVolumeCacheCallback*</b>


          A pointer to the disk cleanup manager's <a href="https://msdn.microsoft.com/d6775458-3b39-4ee8-90f9-d8a749bd1800">IEmptyVolumeCacheCallback</a> interface. This pointer can be used to call that interface's <a href="https://msdn.microsoft.com/41ebc9db-d402-47d7-b303-f87357ae820d">ScanProgress</a> method to report on the progress of the operation.
        


#### - pdwSpaceUsed [out]

Type: <b>DWORDLONG*</b>

The amount of disk space, in bytes, that the handler can free. This value will be displayed in the disk cleanup manager's list, to the right of the handler's check box. To indicate that you do not know how much disk space can be freed, set this parameter to -1, and "???MB" will be displayed. If you set the <b>EVCF_DONTSHOWIFZERO</b> flag when <a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a> was called, setting <i>pdwSpaceUsed</i> to zero will notify the disk cleanup manager to omit the handler from its list. 


## -returns



Type: <b>HRESULT</b>

This method can return one of these values.

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
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
An error occurred when the handler tried to calculate the amount of disk space that could be freed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ABORT</b></dt>
</dl>
</td>
<td width="60%">

            The scan operation was ended prematurely. This value is usually returned when a call to <a href="https://msdn.microsoft.com/41ebc9db-d402-47d7-b303-f87357ae820d">ScanProgress</a> returns E_ABORT. This return value indicates that the user canceled the operation by clicking the disk cleanup manager's <b>Cancel</b> button.
          

</td>
</tr>
</table>
 




## -remarks




        When this method is called by the disk cleanup manager, the handler should start scanning its files to determine which of them can be deleted, and how much disk space will be freed. Handlers should call <a href="https://msdn.microsoft.com/41ebc9db-d402-47d7-b303-f87357ae820d">IEmptyVolumeCache::ScanProgress</a> periodically to keep the user informed of the progress of the scan, especially if it will take a long time. Calling this method frequently also allows the handler to determine whether the user has canceled the operation. If <b>ScanProgress</b> returns E_ABORT, the user has canceled the scan. The handler should immediately stop scanning and return E_ABORT.
      


        You should only set the <i>pdwSpaceUsed</i> parameter to -1 as a last resort. The handler is of limited value to a user if they don't know how much space will be freed.
      



