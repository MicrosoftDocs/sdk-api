---
UID: NF:mbnapi.IMbnInterfaceManager.GetInterface
title: IMbnInterfaceManager::GetInterface (mbnapi.h)
author: windows-sdk-content
description: Gets a specific interface.
old-location: mbn\imbninterfacemanager_getinterface.htm
tech.root: mbn
ms.assetid: f44aa20d-7edd-4227-8eca-9aacb19619e8
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetInterface, GetInterface method [Microsoft Broadband Networks], GetInterface method [Microsoft Broadband Networks],IMbnInterfaceManager interface, IMbnInterfaceManager interface [Microsoft Broadband Networks],GetInterface method, IMbnInterfaceManager.GetInterface, IMbnInterfaceManager::GetInterface, mbn.imbninterfacemanager_getinterface, mbnapi/IMbnInterfaceManager::GetInterface
ms.topic: method
f1_keywords: 
 - "mbnapi/IMbnInterfaceManager.GetInterface"
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
 - IMbnInterfaceManager.GetInterface
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMbnInterfaceManager::GetInterface


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Gets a specific interface.


## -parameters




### -param interfaceID [in]

A string that contains the ID of the interface to retrieve.


### -param mbnInterface [out, retval]

Pointer to the address of the <a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nn-mbnapi-imbninterface">IMbnInterface</a> specified by <i>interfaceID</i> or <b>NULL</b> if there is no matching interface.


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
<dt><b>HRESULT_FROM_WIN32(ERROR_NOT_FOUND)</b></dt>
</dl>
</td>
<td width="60%">
There is no available interface matching the specified interface ID.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>mbnInterface</i> parameter is <b>NULL</b>.

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




<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nn-mbnapi-imbninterfacemanager">IMbnInterfaceManager</a>
 

 

