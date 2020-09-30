---
UID: NF:mbnapi.IMbnInterfaceManager.GetInterfaces
title: IMbnInterfaceManager::GetInterfaces (mbnapi.h)
description: Gets a list of all available IMbnInterface objects.
helpviewer_keywords: ["GetInterfaces","GetInterfaces method [Microsoft Broadband Networks]","GetInterfaces method [Microsoft Broadband Networks]","IMbnInterfaceManager interface","IMbnInterfaceManager interface [Microsoft Broadband Networks]","GetInterfaces method","IMbnInterfaceManager.GetInterfaces","IMbnInterfaceManager::GetInterfaces","mbn.imbninterfacemanager_getinterfaces","mbnapi/IMbnInterfaceManager::GetInterfaces"]
old-location: mbn\imbninterfacemanager_getinterfaces.htm
tech.root: mbn
ms.assetid: 1cd10189-8f36-4bcb-95e9-35064e70fdf8
ms.date: 12/05/2018
ms.keywords: GetInterfaces, GetInterfaces method [Microsoft Broadband Networks], GetInterfaces method [Microsoft Broadband Networks],IMbnInterfaceManager interface, IMbnInterfaceManager interface [Microsoft Broadband Networks],GetInterfaces method, IMbnInterfaceManager.GetInterfaces, IMbnInterfaceManager::GetInterfaces, mbn.imbninterfacemanager_getinterfaces, mbnapi/IMbnInterfaceManager::GetInterfaces
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
 - IMbnInterfaceManager::GetInterfaces
 - mbnapi/IMbnInterfaceManager::GetInterfaces
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
 - IMbnInterfaceManager.GetInterfaces
---

# IMbnInterfaceManager::GetInterfaces


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Gets a list of all available <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbninterface">IMbnInterface</a> objects.

## -parameters

### -param mbnInterfaces [out, retval]

An array of <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbninterface">IMbnInterface</a> interfaces that are associated with the device.  If this method returns anything other than <b>S_OK</b>, then this is <b>NULL</b>.  Otherwise the calling application must free the allocated memory by calling <a href="/windows/win32/api/oleauto/nf-oleauto-safearraydestroy">SafeArrayDestroy</a>.

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
The <i>mbnInterfaces</i> parameter is <b>NULL</b>.

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

<a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbninterfacemanager">IMbnInterfaceManager</a>