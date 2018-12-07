---
UID: NF:shlwapi.SHRegSetValue
title: SHRegSetValue function
author: windows-sdk-content
description: Not supported.
old-location: shell\SHRegSetValue.htm
tech.root: shell
ms.assetid: 64accb02-0d1f-47bf-bc3c-2db7688764f1
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: HKEY_CLASSES_ROOT, HKEY_CURRENT_CONFIG, HKEY_CURRENT_USER, HKEY_LOCAL_MACHINE, HKEY_PERFORMANCE_DATA, HKEY_USERS, SHRegSetValue, SHRegSetValue function [Windows Shell], _shell_SHRegSetValue, shell.SHRegSetValue, shlwapi/SHRegSetValue
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: shlwapi.h
req.include-header: Shlwapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.dll: Shlwapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shlwapi.dll
api_name:
 - SHRegSetValue
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SHRegSetValue function


## -description


Not supported.

Sets a registry value.

Use <a href="https://msdn.microsoft.com/f99774d4-575b-43a3-8887-e15acb0477fd">RegSetValue</a> in its place.


## -parameters




### -param hkey [in]

Type: <b>HKEY</b>

A handle to the currently open key, or any of the following predefined values.

<a id="HKEY_CLASSES_ROOT"></a>
<a id="hkey_classes_root"></a>


#### HKEY_CLASSES_ROOT

<a id="HKEY_CURRENT_CONFIG"></a>
<a id="hkey_current_config"></a>


#### HKEY_CURRENT_CONFIG

<a id="HKEY_CURRENT_USER"></a>
<a id="hkey_current_user"></a>


#### HKEY_CURRENT_USER

<a id="HKEY_LOCAL_MACHINE"></a>
<a id="hkey_local_machine"></a>


#### HKEY_LOCAL_MACHINE

<a id="HKEY_PERFORMANCE_DATA"></a>
<a id="hkey_performance_data"></a>


#### HKEY_PERFORMANCE_DATA

<a id="HKEY_USERS"></a>
<a id="hkey_users"></a>


#### HKEY_USERS


### -param pszSubKey [in]

Type: <b>LPCWSTR</b>

A pointer to a null-terminated string that specifies the relative path from <i>hkey</i> to the subkey from which to retrieve the value. This parameter can be <b>NULL</b> or an empty string, in which case the data is retrieved from the <i>hkey</i> location.


### -param pszValue [in]

Type: <b>LPCWSTR</b>

A pointer to a null-terminated string that contains the name of the value. This parameter can be <b>NULL</b> or an empty string, in which case the data is retrieved from the Default value.


### -param srrfFlags [in]

Type: <b><a href="https://msdn.microsoft.com/c9dbffd1-3b3e-4a25-89ee-1666e2812a62">SRRF</a></b>

One or more of the <a href="https://msdn.microsoft.com/c9dbffd1-3b3e-4a25-89ee-1666e2812a62">SRRF</a> flags that restricts the data to be set. At least one type restriction (SRRF_RT) value must be specified.


### -param dwType [in]

Type: <b>DWORD</b>

The <b>DWORD</b> that indicates the type of data stored in the value to be set. When using default values, the input <i>dwType</i> is the type of the default value. For possible values, see <a href="https://msdn.microsoft.com/4185e7af-e1f0-40af-91c7-0ff7e27896ae">Registry Data Types</a>. If the SRRF_NOEXPAND flag is not set, REG_EXPAND_SZ types are automatically expanded and returned as REG_SZ. If type information is not required, this parameter can be <b>NULL</b>.


### -param pvData [in]

Type: <b>LPCVOID</b>

A pointer to a buffer that contains the value's data. This parameter can be <b>NULL</b> if the data is not needed.


### -param cbData [in]

Type: <b>DWORD</b>

The size of the source data buffer <i>pvData</i>, in bytes. This value can be <b>NULL</b> only if <i>pvData</i> is <b>NULL</b>.


## -returns



Type: <b>LONG</b>

Returns ERROR_SUCCESS if successful, or a nonzero error code defined in Winerror.h otherwise. You can use the <a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> function with the <b>FORMAT_MESSAGE_FROM_SYSTEM</b> flag to retrieve a generic description of the error.




## -see-also




<a href="https://msdn.microsoft.com/e27d2dd6-b139-4ac1-8dd8-527022333364">RegSetKeyValue</a>
 

 

