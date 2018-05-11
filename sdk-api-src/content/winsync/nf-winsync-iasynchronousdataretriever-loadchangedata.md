---
UID: NF:winsync.IAsynchronousDataRetriever.LoadChangeData
title: IAsynchronousDataRetriever::LoadChangeData
author: windows-driver-content
description: Retrieves item data for a change.
old-location: winsync\iasynchronousdataretriever_loadchangedata.htm
old-project: winsync
ms.assetid: b5e73504-1f9e-4a58-9bd9-2c184372b970
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: IAsynchronousDataRetriever interface [Windows Sync],LoadChangeData method, IAsynchronousDataRetriever.LoadChangeData, IAsynchronousDataRetriever::LoadChangeData, LoadChangeData, LoadChangeData method [Windows Sync], LoadChangeData method [Windows Sync],IAsynchronousDataRetriever interface, winsync.iasynchronousdataretriever_loadchangedata, winsync/IAsynchronousDataRetriever::LoadChangeData
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
req.typenames: KNOWLEDGE_COOKIE_COMPARISON_RESULT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	winsync.h
api_name:
-	IAsynchronousDataRetriever.LoadChangeData
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IAsynchronousDataRetriever::LoadChangeData


## -description


Retrieves item data for a change.


## -parameters




### -param pLoadChangeContext [in]

Metadata that describes the change for which data should be retrieved.


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
<td width="60%">
See Remarks.

</td>
</tr>
</table>
 




## -remarks



When <b>LoadChangeData</b> is called, the provider must take one of the following actions:

<ul>
<li>Return a success code from the method and later call <a href="https://msdn.microsoft.com/b48f9a91-f211-4df4-b315-dfe8d48b3db7">IDataRetrieverCallback::LoadChangeDataComplete</a> to report that asynchronous processing finished successfully.</li>
<li>Return a success code from the method and later call <a href="https://msdn.microsoft.com/93185b3d-458d-4254-af2d-02cf7b1c5be7">IDataRetrieverCallback::LoadChangeDataError</a> to report that an error occurred during asynchronous processing.</li>
<li>Return an error code from the method. In this case, <a href="https://msdn.microsoft.com/fc49614d-fdd7-433a-a942-f442edf1c69f">IDataRetrieverCallback</a> methods should not be called.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/38f07582-908b-430e-a886-c0fc24b807ef">IAsynchronousDataRetriever Interface</a>



<a href="https://msdn.microsoft.com/fc49614d-fdd7-433a-a942-f442edf1c69f">IDataRetrieverCallback Interface</a>
 

 

