---
UID: NF:winsync.IDataRetrieverCallback.LoadChangeDataError
title: IDataRetrieverCallback::LoadChangeDataError (winsync.h)
description: Indicates that an IAsynchronousDataRetriever method failed.
helpviewer_keywords: ["IDataRetrieverCallback interface [Windows Sync]","LoadChangeDataError method","IDataRetrieverCallback.LoadChangeDataError","IDataRetrieverCallback::LoadChangeDataError","LoadChangeDataError","LoadChangeDataError method [Windows Sync]","LoadChangeDataError method [Windows Sync]","IDataRetrieverCallback interface","winsync.idataretrievercallback_loadchangedataerror","winsync/IDataRetrieverCallback::LoadChangeDataError"]
old-location: winsync\idataretrievercallback_loadchangedataerror.htm
tech.root: winsync
ms.assetid: 93185b3d-458d-4254-af2d-02cf7b1c5be7
ms.date: 12/05/2018
ms.keywords: IDataRetrieverCallback interface [Windows Sync],LoadChangeDataError method, IDataRetrieverCallback.LoadChangeDataError, IDataRetrieverCallback::LoadChangeDataError, LoadChangeDataError, LoadChangeDataError method [Windows Sync], LoadChangeDataError method [Windows Sync],IDataRetrieverCallback interface, winsync.idataretrievercallback_loadchangedataerror, winsync/IDataRetrieverCallback::LoadChangeDataError
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
 - IDataRetrieverCallback::LoadChangeDataError
 - winsync/IDataRetrieverCallback::LoadChangeDataError
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Winsync.h
api_name:
 - IDataRetrieverCallback.LoadChangeDataError
---

# IDataRetrieverCallback::LoadChangeDataError


## -description

Indicates that an <b>IAsynchronousDataRetriever</b> method failed.

## -parameters

### -param hrError [in]

The error code that represents the reason for the failure.

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
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-idataretrievercallback">IDataRetrieverCallback Interface</a>