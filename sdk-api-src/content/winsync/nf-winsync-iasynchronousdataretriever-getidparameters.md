---
UID: NF:winsync.IAsynchronousDataRetriever.GetIdParameters
title: IAsynchronousDataRetriever::GetIdParameters (winsync.h)
description: Gets the ID format schema of the provider. (IAsynchronousDataRetriever.GetIdParameters)
helpviewer_keywords: ["GetIdParameters","GetIdParameters method [Windows Sync]","GetIdParameters method [Windows Sync]","IAsynchronousDataRetriever interface","IAsynchronousDataRetriever interface [Windows Sync]","GetIdParameters method","IAsynchronousDataRetriever.GetIdParameters","IAsynchronousDataRetriever::GetIdParameters","winsync.iasynchronousdataretriever_getidparameters","winsync/IAsynchronousDataRetriever::GetIdParameters"]
old-location: winsync\iasynchronousdataretriever_getidparameters.htm
tech.root: winsync
ms.assetid: 20f42e0d-dacb-4362-843b-8bc2fb664203
ms.date: 12/05/2018
ms.keywords: GetIdParameters, GetIdParameters method [Windows Sync], GetIdParameters method [Windows Sync],IAsynchronousDataRetriever interface, IAsynchronousDataRetriever interface [Windows Sync],GetIdParameters method, IAsynchronousDataRetriever.GetIdParameters, IAsynchronousDataRetriever::GetIdParameters, winsync.iasynchronousdataretriever_getidparameters, winsync/IAsynchronousDataRetriever::GetIdParameters
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAsynchronousDataRetriever::GetIdParameters
 - winsync/IAsynchronousDataRetriever::GetIdParameters
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - winsync.h
api_name:
 - IAsynchronousDataRetriever.GetIdParameters
---

# IAsynchronousDataRetriever::GetIdParameters


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

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-iasynchronousdataretriever">IAsynchronousDataRetriever Interface</a>
