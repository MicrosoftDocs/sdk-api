---
UID: NF:clusapi.GetCurrentClusterNodeId
title: GetCurrentClusterNodeId macro (clusapi.h)
description: Returns the unique identifier of the current cluster node.
helpviewer_keywords: ["GetCurrentClusterNodeId","GetCurrentClusterNodeId macro [Failover Cluster]","clusapi/GetCurrentClusterNodeId","mscs.getcurrentclusternodeid"]
old-location: mscs\getcurrentclusternodeid.htm
tech.root: MsCS
ms.assetid: 289abaaa-d063-4e99-91e7-441c58f7f75c
ms.date: 07/01/2025
ms.keywords: GetCurrentClusterNodeId, GetCurrentClusterNodeId macro [Failover Cluster], clusapi/GetCurrentClusterNodeId, mscs.getcurrentclusternodeid
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetCurrentClusterNodeId
 - clusapi/GetCurrentClusterNodeId
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ClusAPI.h
api_name:
 - GetCurrentClusterNodeId
---

## -description

Returns the unique identifier of the current cluster <a href="/previous-versions/windows/desktop/mscs/nodes">node</a>.

## -parameters

### -param _lpszNodeId_ [out]

This parameter points to a buffer that receives the unique ID of <i>hNode</i>, including the terminating <b>NULL</b> character.

### -param _lpcchName_ [in, out]

On input, pointer to the count of characters in the buffer pointed to by the <i>lpszNodeId</i> parameter, including the <b>NULL</b> terminator. On output, pointer to the count of characters stored in the buffer excluding the <b>NULL</b> terminator.

## -remarks

Note that <i>_lpcchName_</i> refers to a count of characters and not a count of bytes, and that the returned size does not include the terminating <b>NULL</b> in the count. For more information on sizing buffers, see <a href="/previous-versions/windows/desktop/mscs/data-size-conventions">Data size conventions</a>.

## -see-also

<a href="/windows/win32/api/clusapi/nf-clusapi-getclusternodeid">GetClusterNodeId</a>

<a href="/previous-versions/windows/desktop/mscs/node-management-functions">Node Management Functions</a>

<a href="/windows/win32/api/clusapi/nf-clusapi-openclusternode">OpenClusterNode</a>


## -syntax

```cpp
DWORD GetCurrentClusterNodeId(
  [out]      LPWSTR _lpszNodeId,
  [in, out]  LPDWORD _lpcchName_
);
```

## -returns

Type: **[DWORD](/windows/desktop/winprog/windows-data-types)**

This function returns a [system error code](/windows/win32/debug/system-error-codes). The following are the possible values:

- **ERROR_SUCCESS**
  - 0 (0x0)
  - The operation completed successfully.
- **ERROR_MORE_DATA**
  - 234 (0xEA)
  - More data is available.
  - This value is returned if the buffer pointed to by _\_lpszNodeId_\_ is not long enough to hold the required number of characters. **GetCurrentClusterNodeId** sets the content of _\_lpcchName_\_ to the required length.