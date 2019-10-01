---
UID: NF:winsync.ISynchronousDataRetriever.GetIdParameters
title: ISynchronousDataRetriever::GetIdParameters (winsync.h)
author: windows-sdk-content
description: Gets the ID format schema of the provider.
old-location: winsync\isynchronousdataretriever_getidparameters.htm
tech.root: winsync
ms.assetid: 98273eec-93fd-44ae-a1c9-cf85790dfc1d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetIdParameters, GetIdParameters method [Windows Sync], GetIdParameters method [Windows Sync],ISynchronousDataRetriever interface, ISynchronousDataRetriever interface [Windows Sync],GetIdParameters method, ISynchronousDataRetriever.GetIdParameters, ISynchronousDataRetriever::GetIdParameters, winsync.isynchronousdataretriever_getidparameters, winsync/ISynchronousDataRetriever::GetIdParameters
ms.topic: method
f1_keywords: 
 - "winsync/ISynchronousDataRetriever.GetIdParameters"
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
 - ISynchronousDataRetriever.GetIdParameters
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISynchronousDataRetriever::GetIdParameters


## -description


Gets the ID format schema of the provider.


## -parameters




### -param pIdParameters [out]

Returns the ID format schema of the provider.


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




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nn-winsync-isynchronousdataretriever">ISynchronousDataRetriever Interface</a>
 

 

