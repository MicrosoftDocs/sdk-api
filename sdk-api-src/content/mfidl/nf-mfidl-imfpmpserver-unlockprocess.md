---
UID: NF:mfidl.IMFPMPServer.UnlockProcess
title: IMFPMPServer::UnlockProcess (mfidl.h)
description: Decrements the lock count on the protected media path (PMP) process. Call this method once for each call to IMFPMPServer::LockProcess.
helpviewer_keywords: ["2f64252f-c08b-4624-8df6-db922a630891","IMFPMPServer interface [Media Foundation]","UnlockProcess method","IMFPMPServer.UnlockProcess","IMFPMPServer::UnlockProcess","UnlockProcess","UnlockProcess method [Media Foundation]","UnlockProcess method [Media Foundation]","IMFPMPServer interface","mf.imfpmpserver_unlockprocess","mfidl/IMFPMPServer::UnlockProcess"]
old-location: mf\imfpmpserver_unlockprocess.htm
tech.root: mf
ms.assetid: 2f64252f-c08b-4624-8df6-db922a630891
ms.date: 12/05/2018
ms.keywords: 2f64252f-c08b-4624-8df6-db922a630891, IMFPMPServer interface [Media Foundation],UnlockProcess method, IMFPMPServer.UnlockProcess, IMFPMPServer::UnlockProcess, UnlockProcess, UnlockProcess method [Media Foundation], UnlockProcess method [Media Foundation],IMFPMPServer interface, mf.imfpmpserver_unlockprocess, mfidl/IMFPMPServer::UnlockProcess
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
 - IMFPMPServer::UnlockProcess
 - mfidl/IMFPMPServer::UnlockProcess
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
 - IMFPMPServer.UnlockProcess
---

# IMFPMPServer::UnlockProcess


## -description

Decrements the lock count on the protected media path (PMP) process. Call this method once for each call to <a href="/windows/desktop/api/mfidl/nf-mfidl-imfpmpserver-lockprocess">IMFPMPServer::LockProcess</a>.



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

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfpmpserver">IMFPMPServer</a>
