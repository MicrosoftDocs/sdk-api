---
UID: NF:winsync.IDataRetrieverCallback.LoadChangeDataError
title: IDataRetrieverCallback::LoadChangeDataError
author: windows-sdk-content
description: Indicates that an IAsynchronousDataRetriever method failed.
old-location: winsync\idataretrievercallback_loadchangedataerror.htm
tech.root: winsync
ms.assetid: 93185b3d-458d-4254-af2d-02cf7b1c5be7
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDataRetrieverCallback interface [Windows Sync],LoadChangeDataError method, IDataRetrieverCallback.LoadChangeDataError, IDataRetrieverCallback::LoadChangeDataError, LoadChangeDataError, LoadChangeDataError method [Windows Sync], LoadChangeDataError method [Windows Sync],IDataRetrieverCallback interface, winsync.idataretrievercallback_loadchangedataerror, winsync/IDataRetrieverCallback::LoadChangeDataError
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
 - Winsync.h
api_name:
 - IDataRetrieverCallback.LoadChangeDataError
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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




<a href="https://msdn.microsoft.com/fc49614d-fdd7-433a-a942-f442edf1c69f">IDataRetrieverCallback Interface</a>
 

 

