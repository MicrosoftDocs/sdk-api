---
UID: NF:clusapi.ClusterRegGetKeySecurity
title: ClusterRegGetKeySecurity function (clusapi.h)
description: Returns a copy of the security descriptor protecting the specified cluster database key.
helpviewer_keywords: ["ClusterRegGetKeySecurity","ClusterRegGetKeySecurity function [Failover Cluster]","_wolf_clusterreggetkeysecurity","clusapi/ClusterRegGetKeySecurity","mscs.clusterreggetkeysecurity"]
old-location: mscs\clusterreggetkeysecurity.htm
tech.root: MsCS
ms.assetid: cd0fcfd2-21e0-4627-9b01-6a7f61a80823
ms.date: 12/05/2018
ms.keywords: ClusterRegGetKeySecurity, ClusterRegGetKeySecurity function [Failover Cluster], _wolf_clusterreggetkeysecurity, clusapi/ClusterRegGetKeySecurity, mscs.clusterreggetkeysecurity
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
req.lib: ClusAPI.lib
req.dll: ClusAPI.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ClusterRegGetKeySecurity
 - clusapi/ClusterRegGetKeySecurity
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ClusAPI.dll
api_name:
 - ClusterRegGetKeySecurity
---

# ClusterRegGetKeySecurity function


## -description

Returns a copy of the security descriptor protecting the specified  <a href="/previous-versions/windows/desktop/mscs/cluster-database">cluster database</a> key.

## -parameters

### -param hKey [in]

Handle to a cluster database key.

### -param RequestedInformation [in]

A  <a href="/windows/desktop/SecAuthZ/security-information">SECURITY_INFORMATION</a> structure that indicates the requested security descriptor.

### -param pSecurityDescriptor [out]

Pointer to a <a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a> structure containing a copy of the requested security descriptor.

### -param lpcbSecurityDescriptor [in, out]

On input, pointer to a count of the number of bytes in the buffer pointed to by <i>pSecurityDescriptor</i>. On output, pointer to a count of the number of bytes written to the buffer.

## -returns

If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="/windows/desktop/Debug/system-error-codes">system error code</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterregopenkey">ClusterRegOpenKey</a>