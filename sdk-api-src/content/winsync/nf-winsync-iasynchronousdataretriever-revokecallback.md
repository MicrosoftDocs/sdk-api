---
UID: NF:winsync.IAsynchronousDataRetriever.RevokeCallback
title: IAsynchronousDataRetriever::RevokeCallback (winsync.h)
description: Indicates that the IAsynchronousDataRetriever object must no longer use the specified callback interface and must release any references to it.
helpviewer_keywords: ["IAsynchronousDataRetriever interface [Windows Sync]","RevokeCallback method","IAsynchronousDataRetriever.RevokeCallback","IAsynchronousDataRetriever::RevokeCallback","RevokeCallback","RevokeCallback method [Windows Sync]","RevokeCallback method [Windows Sync]","IAsynchronousDataRetriever interface","winsync.iasynchronousdataretriever_revokecallback","winsync/IAsynchronousDataRetriever::RevokeCallback"]
old-location: winsync\iasynchronousdataretriever_revokecallback.htm
tech.root: winsync
ms.assetid: bb7b1457-03aa-47e0-9e61-6195706a0fcd
ms.date: 12/05/2018
ms.keywords: IAsynchronousDataRetriever interface [Windows Sync],RevokeCallback method, IAsynchronousDataRetriever.RevokeCallback, IAsynchronousDataRetriever::RevokeCallback, RevokeCallback, RevokeCallback method [Windows Sync], RevokeCallback method [Windows Sync],IAsynchronousDataRetriever interface, winsync.iasynchronousdataretriever_revokecallback, winsync/IAsynchronousDataRetriever::RevokeCallback
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
 - IAsynchronousDataRetriever::RevokeCallback
 - winsync/IAsynchronousDataRetriever::RevokeCallback
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
 - IAsynchronousDataRetriever.RevokeCallback
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

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-iasynchronousdataretriever">IAsynchronousDataRetriever Interface</a>