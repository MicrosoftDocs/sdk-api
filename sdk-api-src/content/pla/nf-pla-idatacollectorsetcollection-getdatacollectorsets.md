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

# IDataCollectorSetCollection::GetDataCollectorSets


## -description


Populates the data collector set collection.


## -parameters




### -param server




### -param filter






#### - pFilter [in]

If empty, PLA enumerates sets from all namespaces; otherwise, specify a specific namespace to enumerate. The form is &lt;namespace&gt;\*. For possible namespace values, see <a href="https://msdn.microsoft.com/7e432e1f-4b86-45dc-93d5-df603068273d">IDataCollectorSet::Commit</a>.


#### - pServer [in]

The computer whose data collector sets you want to enumerate. You can specify a computer name, a fully qualified domain name, or an IP address (IPv4 or IPv6 format). If <b>NULL</b>, PLA enumerates the sets on the local computer.


## -returns



Returns S_OK if successful. The following table shows possible error values.

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
The RPC server is not available. The method is unable to query the data collector set remotely. To query the data collector set from a remote computer running Windows Vista, enable Performance Logs and Alerts in <b>Windows Firewall Settings</b> on the remote computer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_BAD_NETPATH)</b></dt>
</dl>
</td>
<td width="60%">
Unable to find the remote computer.

</td>
</tr>
</table>
 




## -remarks



The method enumerates only those sets that have been previously saved using <a href="https://msdn.microsoft.com/7e432e1f-4b86-45dc-93d5-df603068273d">IDataCollectorSet::Commit</a>.

 The retrieved data collector sets overwrite the contents of this instance. The instance must be empty (newly created) or be from the same namespace.




## -see-also




<a href="https://msdn.microsoft.com/5f4cc411-1efb-4f70-a677-3c20d95f0c53">IDataCollectorSetCollection</a>
 

 

