---
UID: NF:clusapi.ClusterRegSetValue
title: ClusterRegSetValue function
author: windows-sdk-content
description: Sets a value for a cluster database key.
old-location: mscs\clusterregsetvalue.htm
tech.root: mscs
ms.assetid: 6e4fee56-1c18-4f6d-81ae-c305aae59572
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: ClusterRegSetValue, ClusterRegSetValue function [Failover Cluster], REG_BINARY, REG_DWORD, REG_DWORD_BIG_ENDIAN, REG_EXPAND_SZ, REG_MULTI_SZ, REG_NONE, REG_QWORD, REG_SZ, _wolf_clusterregsetvalue, clusapi/ClusterRegSetValue, mscs.clusterregsetvalue
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: ClusAPI.lib
req.dll: ClusAPI.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ClusAPI.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-1.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-2.dll
api_name:
 - ClusterRegSetValue
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ClusterRegSetValue function


## -description


Sets a value for a 
    <a href="https://msdn.microsoft.com/d2c1a9c0-7e87-4a3c-9a1a-7f1756f97804">cluster database</a> key.


## -parameters




### -param hKey [in]

Handle to a cluster database key.


### -param lpszValueName [in]

Pointer to a null-terminated Unicode string containing the name of the value to set. If a value with this 
       name is not already present in the <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resource</a>, 
       <b>ClusterRegSetValue</b> adds it to the resource.


### -param dwType [in]

Type of information to be stored as the value's data. This parameter can be one of the following values. For more information see <a href="https://msdn.microsoft.com/5fd828d6-4d62-4823-a2f1-15782b5cd28c">Registry Value Types</a>.



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
      <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>.




## -remarks



Do not call <b>ClusterRegSetValue</b> from the 
     following resource DLL entry point functions:


<ul>
<li>
<a href="https://msdn.microsoft.com/c7c74440-c98a-4440-8bf4-10ebd1a68608">Close</a>
</li>
<li>
<a href="https://msdn.microsoft.com/1d67a4f5-66f8-4818-8b63-d0f50452f889">Offline</a>
</li>
<li>
<a href="https://msdn.microsoft.com/b406ef44-0622-4625-a6cf-462b6ea6018d">Online</a>
</li>
<li>
<a href="https://msdn.microsoft.com/0a5c10c5-0380-4638-b49d-396be3b3c0dd">Open</a>
</li>
<li>
<a href="https://msdn.microsoft.com/b53ab7db-ed17-4386-8a5f-5d0b0d1cb1b3">Terminate</a>
</li>
</ul>


<b>ClusterRegSetValue</b> can be safely called from any 
     other resource DLL entry point function or from a worker thread. For more information, see 
     <a href="https://msdn.microsoft.com/0eaa4aea-8d9a-4552-b43a-fafa23a3e736">Function Calls to Avoid in Resource DLLs</a>.




## -see-also




<a href="https://msdn.microsoft.com/f2cf204e-d02d-40b9-86d7-0262b8cc4db1">ClusterRegOpenKey</a>



<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>
 

 

