---
UID: NF:mbnapi.IMbnInterfaceManager.GetInterfaces
title: IMbnInterfaceManager::GetInterfaces
author: windows-sdk-content
description: Gets a list of all available IMbnInterface objects.
old-location: mbn\imbninterfacemanager_getinterfaces.htm
tech.root: mbn
ms.assetid: 1cd10189-8f36-4bcb-95e9-35064e70fdf8
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: GetInterfaces, GetInterfaces method [Microsoft Broadband Networks], GetInterfaces method [Microsoft Broadband Networks],IMbnInterfaceManager interface, IMbnInterfaceManager interface [Microsoft Broadband Networks],GetInterfaces method, IMbnInterfaceManager.GetInterfaces, IMbnInterfaceManager::GetInterfaces, mbn.imbninterfacemanager_getinterfaces, mbnapi/IMbnInterfaceManager::GetInterfaces
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
 - IMbnInterfaceManager.GetInterfaces
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMbnInterfaceManager::GetInterfaces


## -description


Gets a list of all available <a href="https://msdn.microsoft.com/958bce42-4772-4706-8900-1f83c5d3d52b">IMbnInterface</a> objects.


## -parameters




### -param mbnInterfaces [out, retval]

An array of <a href="https://msdn.microsoft.com/958bce42-4772-4706-8900-1f83c5d3d52b">IMbnInterface</a> interfaces that are associated with the device.  If this method returns anything other than <b>S_OK</b>, then this is <b>NULL</b>.  Otherwise the calling application must free the allocated memory by calling <a href="http://go.microsoft.com/fwlink/p/?linkid=121490">SafeArrayDestroy</a>.


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




<a href="https://msdn.microsoft.com/a998381e-47de-4352-bc84-b6edca2f3fcc">IMbnInterfaceManager</a>
 

 

