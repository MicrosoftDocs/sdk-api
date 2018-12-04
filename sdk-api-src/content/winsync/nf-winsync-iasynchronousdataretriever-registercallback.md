---
UID: NF:winsync.IAsynchronousDataRetriever.RegisterCallback
title: IAsynchronousDataRetriever::RegisterCallback
author: windows-sdk-content
description: Registers a callback interface that will be called by the IAsynchronousDataRetriever object when an asynchronous method finishes processing.
old-location: winsync\iasynchronousdataretriever_registercallback.htm
tech.root: winsync
ms.assetid: 4148db4a-a460-40ca-863a-861065f89c5c
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IAsynchronousDataRetriever interface [Windows Sync],RegisterCallback method, IAsynchronousDataRetriever.RegisterCallback, IAsynchronousDataRetriever::RegisterCallback, RegisterCallback, RegisterCallback method [Windows Sync], RegisterCallback method [Windows Sync],IAsynchronousDataRetriever interface, winsync.iasynchronousdataretriever_registercallback, winsync/IAsynchronousDataRetriever::RegisterCallback
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
 - IAsynchronousDataRetriever.RegisterCallback
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAsynchronousDataRetriever::RegisterCallback


## -description


Registers a callback interface that will be called by the <b>IAsynchronousDataRetriever</b> object when an asynchronous method finishes processing.


## -parameters




### -param pDataRetrieverCallback [in]

The callback interface to register.


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
 

 

