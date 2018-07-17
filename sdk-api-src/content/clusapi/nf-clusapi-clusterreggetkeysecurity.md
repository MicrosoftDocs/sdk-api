---
UID: NF:clusapi.ClusterRegGetKeySecurity
title: ClusterRegGetKeySecurity function
author: windows-sdk-content
description: Returns a copy of the security descriptor protecting the specified cluster database key.
old-location: mscs\clusterreggetkeysecurity.htm
old-project: mscs
ms.assetid: cd0fcfd2-21e0-4627-9b01-6a7f61a80823
ms.author: windowssdkdev
ms.date: 07/12/2018
ms.keywords: ClusterRegGetKeySecurity, ClusterRegGetKeySecurity function [Failover Cluster], _wolf_clusterreggetkeysecurity, clusapi/ClusterRegGetKeySecurity, mscs.clusterreggetkeysecurity
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Enterprise, Windows Server 2008 Datacenter
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: SR_REPLICATED_DISK_TYPE, *PSR_REPLICATED_DISK_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ClusAPI.dll
api_name:
 - ClusterRegGetKeySecurity
product: Windows
targetos: Windows
req.lib: ClusAPI.lib
req.dll: ClusAPI.dll
req.irql: 
---

# ClusterRegGetKeySecurity function


## -description


Returns a copy of the security descriptor protecting the specified  <a href="https://msdn.microsoft.com/d2c1a9c0-7e87-4a3c-9a1a-7f1756f97804">cluster database</a> key.


## -parameters




### -param hKey [in]

Handle to a cluster database key.


### -param RequestedInformation [in]

A  <a href="https://msdn.microsoft.com/library/windows/hardware/ff556635">SECURITY_INFORMATION</a> structure that indicates the requested security descriptor.


### -param pSecurityDescriptor [out]

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff563689">SECURITY_DESCRIPTOR</a> structure containing a copy of the requested security descriptor.


### -param lpcbSecurityDescriptor [in, out]

On input, pointer to a count of the number of bytes in the buffer pointed to by <i>pSecurityDescriptor</i>. On output, pointer to a count of the number of bytes written to the buffer.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>.




## -see-also




<a href="https://msdn.microsoft.com/f2cf204e-d02d-40b9-86d7-0262b8cc4db1">ClusterRegOpenKey</a>
 

 

