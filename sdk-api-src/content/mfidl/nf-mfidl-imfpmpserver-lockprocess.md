---
UID: NF:mfidl.IMFPMPServer.LockProcess
title: IMFPMPServer::LockProcess
author: windows-sdk-content
description: Blocks the protected media path (PMP) process from ending.
old-location: mf\imfpmpserver_lockprocess.htm
old-project: medfound
ms.assetid: 9a25abfb-5038-4869-ad70-1ae52e8cf599
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: 9a25abfb-5038-4869-ad70-1ae52e8cf599, IMFPMPServer interface [Media Foundation],LockProcess method, IMFPMPServer.LockProcess, IMFPMPServer::LockProcess, LockProcess, LockProcess method [Media Foundation], LockProcess method [Media Foundation],IMFPMPServer interface, mf.imfpmpserver_lockprocess, mfidl/IMFPMPServer::LockProcess
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mfidl.h
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
tech.root: 
req.typenames: MFSensorDeviceMode
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFPMPServer.LockProcess
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFPMPServer::LockProcess


## -description



Blocks the protected media path (PMP) process from ending.




## -parameters






## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The method succeeded.

</td>
</tr>
</table>
 




## -remarks



When this method is called, it increments the lock count on the PMP process. For every call to this method, the application should make a corresponding call to <a href="https://msdn.microsoft.com/2f64252f-c08b-4624-8df6-db922a630891">IMFPMPServer::UnlockProcess</a>, which decrements the lock count. When the PMP process is ready to exit, it waits for about 3 seconds, or until the lock count reaches zero, before exiting.




## -see-also




<a href="https://msdn.microsoft.com/ba6dc70a-d77d-41de-afe1-65f2efcc4a95">IMFPMPServer</a>
 

 

