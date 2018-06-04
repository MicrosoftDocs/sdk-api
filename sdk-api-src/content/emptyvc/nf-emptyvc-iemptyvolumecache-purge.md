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

# IEmptyVolumeCache::Purge


## -description


Notifies the handler to start deleting its unneeded files.


## -parameters




### -param dwlSpaceToFree




### -param picb [in]

Type: <b>IEmptyVolumeCacheCallback*</b>

A pointer to the disk cleanup manager's <a href="https://msdn.microsoft.com/d6775458-3b39-4ee8-90f9-d8a749bd1800">IEmptyVolumeCacheCallBack</a> interface. This pointer can be used to call the interface's <a href="https://msdn.microsoft.com/96b97919-9b3b-418e-a76a-a2e8aad453b9">PurgeProgress</a> method to report on the progress of the operation. 


#### - dwSpaceToFree [in]

Type: <b>DWORDLONG</b>

The amount of disk space that the handler should free. If this parameter is set to -1, the handler should delete all its files. 


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
<dt><b>E_ABORT</b></dt>
</dl>
</td>
<td width="60%">
The operation was ended prematurely. This value is usually returned when <a href="https://msdn.microsoft.com/96b97919-9b3b-418e-a76a-a2e8aad453b9">PurgeProgress</a> returns E_ABORT. This typically happens when the user cancels the operation by clicking the disk cleanup manager's <b>Cancel</b> button.

</td>
</tr>
</table>
 




## -remarks



For Windows 98, the <i>dwSpaceToFree</i> parameter is always set to the value specified by the handler when <a href="https://msdn.microsoft.com/c8ec2f70-f327-49d4-babb-a9640f105003">IEmptyVolumeCache::GetSpaceUsed</a> was called.

In general, handlers should be kept simple and delete all of their files when this function is called. If there are significant performance advantages to only deleting a portion of the files, the handler should implement the <a href="https://msdn.microsoft.com/3bce6251-b209-405a-8ac2-fd385f1c69ee">ShowProperties</a> method. When called, this method displays a UI that allows the user to select the files to be deleted.



