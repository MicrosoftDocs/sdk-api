---
UID: NF:winsync.IAsynchronousDataRetriever.RevokeCallback
title: IAsynchronousDataRetriever::RevokeCallback
author: windows-sdk-content
description: Indicates that the IAsynchronousDataRetriever object must no longer use the specified callback interface and must release any references to it.
old-location: winsync\iasynchronousdataretriever_revokecallback.htm
tech.root: winsync
ms.assetid: bb7b1457-03aa-47e0-9e61-6195706a0fcd
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IAsynchronousDataRetriever interface [Windows Sync],RevokeCallback method, IAsynchronousDataRetriever.RevokeCallback, IAsynchronousDataRetriever::RevokeCallback, RevokeCallback, RevokeCallback method [Windows Sync], RevokeCallback method [Windows Sync],IAsynchronousDataRetriever interface, winsync.iasynchronousdataretriever_revokecallback, winsync/IAsynchronousDataRetriever::RevokeCallback
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: winsync.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - winsync.h
api_name:
 - IAsynchronousDataRetriever.RevokeCallback
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAsynchronousDataRetriever::RevokeCallback


## -description


Indicates that the <b>IAsynchronousDataRetriever</b> object must no longer use the specified callback interface and must release any references to it.


## -parameters




### -param pDataRetrieverCallback [in]

The callback interface to release.


## -returns



The possible return codes include, but are not limited to, the values shown in the following table.

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
<tr>
<td width="40%">
<dl>
<dt><b>Provider-determined error codes.</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/38f07582-908b-430e-a886-c0fc24b807ef">IAsynchronousDataRetriever Interface</a>
 

 

