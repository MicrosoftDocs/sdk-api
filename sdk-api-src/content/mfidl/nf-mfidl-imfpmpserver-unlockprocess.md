---
UID: NF:mfidl.IMFPMPServer.UnlockProcess
title: IMFPMPServer::UnlockProcess
author: windows-driver-content
description: Decrements the lock count on the protected media path (PMP) process. Call this method once for each call to IMFPMPServer::LockProcess.
old-location: mf\imfpmpserver_unlockprocess.htm
old-project: medfound
ms.assetid: 2f64252f-c08b-4624-8df6-db922a630891
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: 2f64252f-c08b-4624-8df6-db922a630891, IMFPMPServer interface [Media Foundation],UnlockProcess method, IMFPMPServer.UnlockProcess, IMFPMPServer::UnlockProcess, UnlockProcess, UnlockProcess method [Media Foundation], UnlockProcess method [Media Foundation],IMFPMPServer interface, mf.imfpmpserver_unlockprocess, mfidl/IMFPMPServer::UnlockProcess
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: MF_URL_TRUST_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfuuid.lib
-	mfuuid.dll
api_name:
-	IMFPMPServer.UnlockProcess
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFPMPServer::UnlockProcess


## -description



Decrements the lock count on the protected media path (PMP) process. Call this method once for each call to <a href="https://msdn.microsoft.com/9a25abfb-5038-4869-ad70-1ae52e8cf599">IMFPMPServer::LockProcess</a>.




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
 




## -see-also




<a href="https://msdn.microsoft.com/ba6dc70a-d77d-41de-afe1-65f2efcc4a95">IMFPMPServer</a>
 

 

