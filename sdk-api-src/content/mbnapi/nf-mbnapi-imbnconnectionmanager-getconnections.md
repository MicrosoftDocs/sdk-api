---
UID: NF:mbnapi.IMbnConnectionManager.GetConnections
title: IMbnConnectionManager::GetConnections
author: windows-sdk-content
description: Gets a list of available connections.
old-location: mbn\imbnconnectionmanager_getconnections.htm
tech.root: mbn
ms.assetid: 5f4fd3b2-ed24-403a-ae5a-31821a2c7033
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetConnections, GetConnections method [Microsoft Broadband Networks], GetConnections method [Microsoft Broadband Networks],IMbnConnectionManager interface, IMbnConnectionManager interface [Microsoft Broadband Networks],GetConnections method, IMbnConnectionManager.GetConnections, IMbnConnectionManager::GetConnections, mbn.imbnconnectionmanager_getconnections, mbnapi/IMbnConnectionManager::GetConnections
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mbnapi.h
api_name:
 - IMbnConnectionManager.GetConnections
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMbnConnectionManager::GetConnections


## -description


Gets a list of available connections.


## -parameters




### -param mbnConnections [out]

An array of <a href="https://msdn.microsoft.com/dae6ce6f-2534-4799-8ed3-53cd1f2eca13">IMbnConnection</a> interfaces representing connections that are associated with the devices.  If this method returns anything other than <b>S_OK</b>, then this is <b>NULL</b>.  Otherwise the calling application must free the allocated memory by calling <a href="http://go.microsoft.com/fwlink/p/?linkid=121490">SafeArrayDestroy</a>.


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




<a href="https://msdn.microsoft.com/20b9243d-1f20-4092-951a-fbacb2d55481">IMbnConnectionManager</a>
 

 

