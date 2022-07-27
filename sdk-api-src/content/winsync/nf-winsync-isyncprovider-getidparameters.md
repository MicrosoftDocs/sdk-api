---
UID: NF:winsync.ISyncProvider.GetIdParameters
title: ISyncProvider::GetIdParameters (winsync.h)
description: Gets the ID format schema of the provider. (ISyncProvider.GetIdParameters)
helpviewer_keywords: ["GetIdParameters","GetIdParameters method [Windows Sync]","GetIdParameters method [Windows Sync]","ISyncProvider interface","ISyncProvider interface [Windows Sync]","GetIdParameters method","ISyncProvider.GetIdParameters","ISyncProvider::GetIdParameters","winsync.isyncprovider_getidparameters","winsync/ISyncProvider::GetIdParameters"]
old-location: winsync\isyncprovider_getidparameters.htm
tech.root: winsync
ms.assetid: a1839c53-7978-4a14-8b17-43621b801f13
ms.date: 12/05/2018
ms.keywords: GetIdParameters, GetIdParameters method [Windows Sync], GetIdParameters method [Windows Sync],ISyncProvider interface, ISyncProvider interface [Windows Sync],GetIdParameters method, ISyncProvider.GetIdParameters, ISyncProvider::GetIdParameters, winsync.isyncprovider_getidparameters, winsync/ISyncProvider::GetIdParameters
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
 - ISyncProvider::GetIdParameters
 - winsync/ISyncProvider::GetIdParameters
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
 - ISyncProvider.GetIdParameters
---

# ISyncProvider::GetIdParameters


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

## -remarks

This method is used to get the ID format schema from the two providers that are participating in synchronization. A synchronization session should use this method to verify that the two providers have the same ID format schema, so that they can synchronize with one another.

## -see-also

<a href="/windows/desktop/api/winsync/ns-winsync-id_parameters">ID_PARAMETERS Structure</a>



<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncprovider">ISyncProvider Interface</a>
