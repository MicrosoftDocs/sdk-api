---
UID: NF:mbnapi.IMbnConnectionManager.GetConnection
title: IMbnConnectionManager::GetConnection (mbnapi.h)
description: Gets a connection.
helpviewer_keywords: ["GetConnection","GetConnection method [Microsoft Broadband Networks]","GetConnection method [Microsoft Broadband Networks]","IMbnConnectionManager interface","IMbnConnectionManager interface [Microsoft Broadband Networks]","GetConnection method","IMbnConnectionManager.GetConnection","IMbnConnectionManager::GetConnection","mbn.imbnconnectionmanager_getconnection","mbnapi/IMbnConnectionManager::GetConnection"]
old-location: mbn\imbnconnectionmanager_getconnection.htm
tech.root: mbn
ms.assetid: fbeac057-77e3-438e-a7a9-b6f223a09dbe
ms.date: 12/05/2018
ms.keywords: GetConnection, GetConnection method [Microsoft Broadband Networks], GetConnection method [Microsoft Broadband Networks],IMbnConnectionManager interface, IMbnConnectionManager interface [Microsoft Broadband Networks],GetConnection method, IMbnConnectionManager.GetConnection, IMbnConnectionManager::GetConnection, mbn.imbnconnectionmanager_getconnection, mbnapi/IMbnConnectionManager::GetConnection
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mbnapi.idl
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
 - IMbnConnectionManager::GetConnection
 - mbnapi/IMbnConnectionManager::GetConnection
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mbnapi.h
api_name:
 - IMbnConnectionManager.GetConnection
---

# IMbnConnectionManager::GetConnection


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Gets a connection.

## -parameters

### -param connectionID [in]

A string containing the connection ID.

### -param mbnConnection [out, retval]

A pointer to an <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnection">IMbnConnection</a> interface that represents the requested connection.  If the method returns anything other than S_OK, then this is <b>NULL</b>.

## -returns

This method can return one of these values.

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
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>mbnConnection</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Could not allocate the required memory.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectionmanager">IMbnConnectionManager</a>