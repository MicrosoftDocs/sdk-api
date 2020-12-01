---
UID: NF:mbnapi.IMbnConnectionManager.GetConnections
title: IMbnConnectionManager::GetConnections (mbnapi.h)
description: Gets a list of available connections.
helpviewer_keywords: ["GetConnections","GetConnections method [Microsoft Broadband Networks]","GetConnections method [Microsoft Broadband Networks]","IMbnConnectionManager interface","IMbnConnectionManager interface [Microsoft Broadband Networks]","GetConnections method","IMbnConnectionManager.GetConnections","IMbnConnectionManager::GetConnections","mbn.imbnconnectionmanager_getconnections","mbnapi/IMbnConnectionManager::GetConnections"]
old-location: mbn\imbnconnectionmanager_getconnections.htm
tech.root: mbn
ms.assetid: 5f4fd3b2-ed24-403a-ae5a-31821a2c7033
ms.date: 12/05/2018
ms.keywords: GetConnections, GetConnections method [Microsoft Broadband Networks], GetConnections method [Microsoft Broadband Networks],IMbnConnectionManager interface, IMbnConnectionManager interface [Microsoft Broadband Networks],GetConnections method, IMbnConnectionManager.GetConnections, IMbnConnectionManager::GetConnections, mbn.imbnconnectionmanager_getconnections, mbnapi/IMbnConnectionManager::GetConnections
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
 - IMbnConnectionManager::GetConnections
 - mbnapi/IMbnConnectionManager::GetConnections
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
 - IMbnConnectionManager.GetConnections
---

# IMbnConnectionManager::GetConnections


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Gets a list of available connections.

## -parameters

### -param mbnConnections [out]

An array of <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnection">IMbnConnection</a> interfaces representing connections that are associated with the devices.  If this method returns anything other than <b>S_OK</b>, then this is <b>NULL</b>.  Otherwise the calling application must free the allocated memory by calling <a href="/windows/win32/api/oleauto/nf-oleauto-safearraydestroy">SafeArrayDestroy</a>.

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
The <i>mbnConnections</i> parameter is <b>NULL</b>.

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