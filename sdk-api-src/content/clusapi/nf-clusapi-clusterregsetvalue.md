---
UID: NF:clusapi.ClusterRegSetValue
title: ClusterRegSetValue function (clusapi.h)
description: Sets a value for a cluster database key.
helpviewer_keywords: ["ClusterRegSetValue","ClusterRegSetValue function [Failover Cluster]","REG_BINARY","REG_DWORD","REG_DWORD_BIG_ENDIAN","REG_EXPAND_SZ","REG_MULTI_SZ","REG_NONE","REG_QWORD","REG_SZ","_wolf_clusterregsetvalue","clusapi/ClusterRegSetValue","mscs.clusterregsetvalue"]
old-location: mscs\clusterregsetvalue.htm
tech.root: MsCS
ms.assetid: 6e4fee56-1c18-4f6d-81ae-c305aae59572
ms.date: 12/05/2018
ms.keywords: ClusterRegSetValue, ClusterRegSetValue function [Failover Cluster], REG_BINARY, REG_DWORD, REG_DWORD_BIG_ENDIAN, REG_EXPAND_SZ, REG_MULTI_SZ, REG_NONE, REG_QWORD, REG_SZ, _wolf_clusterregsetvalue, clusapi/ClusterRegSetValue, mscs.clusterregsetvalue
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
 - ClusterRegSetValue
 - clusapi/ClusterRegSetValue
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-cluster-clusapi-l1-1-6.dll
 - ext-ms-win-cluster-clusapi-l1-1-5.dll
 - ext-ms-win-cluster-clusapi-l1-1-4.dll
 - ClusAPI.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-1.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-2.dll
 - ext-ms-win-cluster-clusapi-l1-1-3.dll
api_name:
 - ClusterRegSetValue
---

# ClusterRegSetValue function


## -description

Sets a value for a 
    <a href="/previous-versions/windows/desktop/mscs/cluster-database">cluster database</a> key.

## -parameters

### -param hKey [in]

Handle to a cluster database key.

### -param lpszValueName [in]

Pointer to a null-terminated Unicode string containing the name of the value to set. If a value with this 
       name is not already present in the <a href="/previous-versions/windows/desktop/mscs/resources">resource</a>, 
       <b>ClusterRegSetValue</b> adds it to the resource.

### -param dwType [in]

Type of information to be stored as the value's data. This parameter can be one of the following values. For more information see <a href="/windows/desktop/SysInfo/registry-value-types">Registry Value Types</a>.



#### REG_BINARY (3)

Binary data in any form.



#### REG_DWORD (4)

A 32-bit number.



#### REG_DWORD_BIG_ENDIAN (5)

A 32-bit number stored in big-endian format.



#### REG_EXPAND_SZ (2)

A null-terminated Unicode string that contains unexpanded references to environment variables (for example, 
         "%PATH%").



#### REG_MULTI_SZ (6)

A sequence of null-terminated strings, terminated by an empty string (\0).

The following is an example:

<i>String1</i>\0<i>String2</i>\0<i>String3</i>\0<i>LastString</i>\0\0

The first \0 terminates the first string, the second to the last \0 terminates the last string, and the 
         final \0 terminates the sequence. Note that the final terminator must be factored into the length of the 
         string.



#### REG_NONE (0)

No defined value type.



#### REG_QWORD (11)

A 64-bit number.



#### REG_SZ (1)

A null-terminated Unicode string.

### -param lpData [in]

Pointer to the data to be stored with the name pointed to by <i>lpszValueName</i>.

### -param cbData [in]

Count of bytes in the data pointed to by the <i>lpbData</i> parameter. If the data is of 
       type <b>REG_SZ</b>, <b>REG_EXPAND_SZ</b> or 
       <b>REG_MULTI_SZ</b>, <i>cbData</i> must include the size of the 
       null-terminating character.

## -returns

If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, the function returns a 
      <a href="/windows/desktop/Debug/system-error-codes">system error code</a>.

## -remarks

Do not call <b>ClusterRegSetValue</b> from the 
     following resource DLL entry point functions:


<ul>
<li>
<a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-pclose_routine">Close</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-poffline_routine">Offline</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-ponline_routine">Online</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-popen_routine">Open</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-pterminate_routine">Terminate</a>
</li>
</ul>


<b>ClusterRegSetValue</b> can be safely called from any 
     other resource DLL entry point function or from a worker thread. For more information, see 
     <a href="/previous-versions/windows/desktop/mscs/function-calls-to-avoid-in-resource-dlls">Function Calls to Avoid in Resource DLLs</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterregopenkey">ClusterRegOpenKey</a>



<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>