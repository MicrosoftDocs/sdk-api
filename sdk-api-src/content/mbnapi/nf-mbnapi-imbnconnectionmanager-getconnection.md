---
UID: NF:mbnapi.IMbnConnectionManager.GetConnection
title: IMbnConnectionManager::GetConnection (mbnapi.h)
author: windows-sdk-content
description: Gets a connection.
old-location: mbn\imbnconnectionmanager_getconnection.htm
tech.root: mbn
ms.assetid: fbeac057-77e3-438e-a7a9-b6f223a09dbe
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetConnection, GetConnection method [Microsoft Broadband Networks], GetConnection method [Microsoft Broadband Networks],IMbnConnectionManager interface, IMbnConnectionManager interface [Microsoft Broadband Networks],GetConnection method, IMbnConnectionManager.GetConnection, IMbnConnectionManager::GetConnection, mbn.imbnconnectionmanager_getconnection, mbnapi/IMbnConnectionManager::GetConnection
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
 - IMbnConnectionManager.GetConnection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMbnConnectionManager::GetConnection


## -description


Gets a connection.


## -parameters




### -param connectionID [in]

A string containing the connection ID.


### -param mbnConnection [out, retval]

A pointer to an <a href="https://msdn.microsoft.com/dae6ce6f-2534-4799-8ed3-53cd1f2eca13">IMbnConnection</a> interface that represents the requested connection.  If the method returns anything other than S_OK, then this is <b>NULL</b>.


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




<a href="https://msdn.microsoft.com/20b9243d-1f20-4092-951a-fbacb2d55481">IMbnConnectionManager</a>
 

 

