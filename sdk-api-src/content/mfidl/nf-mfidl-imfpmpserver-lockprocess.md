---
UID: NF:mfidl.IMFPMPServer.LockProcess
title: IMFPMPServer::LockProcess (mfidl.h)
description: Blocks the protected media path (PMP) process from ending. (IMFPMPServer.LockProcess)
helpviewer_keywords: ["9a25abfb-5038-4869-ad70-1ae52e8cf599","IMFPMPServer interface [Media Foundation]","LockProcess method","IMFPMPServer.LockProcess","IMFPMPServer::LockProcess","LockProcess","LockProcess method [Media Foundation]","LockProcess method [Media Foundation]","IMFPMPServer interface","mf.imfpmpserver_lockprocess","mfidl/IMFPMPServer::LockProcess"]
old-location: mf\imfpmpserver_lockprocess.htm
tech.root: mf
ms.assetid: 9a25abfb-5038-4869-ad70-1ae52e8cf599
ms.date: 12/05/2018
ms.keywords: 9a25abfb-5038-4869-ad70-1ae52e8cf599, IMFPMPServer interface [Media Foundation],LockProcess method, IMFPMPServer.LockProcess, IMFPMPServer::LockProcess, LockProcess, LockProcess method [Media Foundation], LockProcess method [Media Foundation],IMFPMPServer interface, mf.imfpmpserver_lockprocess, mfidl/IMFPMPServer::LockProcess
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
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFPMPServer::LockProcess
 - mfidl/IMFPMPServer::LockProcess
dev_langs:
 - c++
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
---

# IMFPMPServer::LockProcess


## -description

Blocks the protected media path (PMP) process from ending.



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

When this method is called, it increments the lock count on the PMP process. For every call to this method, the application should make a corresponding call to <a href="/windows/desktop/api/mfidl/nf-mfidl-imfpmpserver-unlockprocess">IMFPMPServer::UnlockProcess</a>, which decrements the lock count. When the PMP process is ready to exit, it waits for about 3 seconds, or until the lock count reaches zero, before exiting.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfpmpserver">IMFPMPServer</a>
