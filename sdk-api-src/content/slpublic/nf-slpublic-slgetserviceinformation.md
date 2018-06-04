---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# SLGetServiceInformation function


## -description


Gets global data information.


## -parameters




### -param hSLC [in]

Type: <b>HSLC</b>

The handle to the current SLC context.


### -param pwszValueName [in]

Type: <b>PCWSTR</b>

The name associated with the value to retrieve.  The following names are valid.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SL_INFO_KEY_VERSION"></a><a id="sl_info_key_version"></a><dl>
<dt><b>SL_INFO_KEY_VERSION</b></dt>
<dt>L"Version"</dt>
</dl>
</td>
<td width="60%">
Version of SL service. e.g. "1.2.3.4"

</td>
</tr>
<tr>
<td width="40%"><a id="SL_INFO_KEY_SYSTEM_STATE"></a><a id="sl_info_key_system_state"></a><dl>
<dt><b>SL_INFO_KEY_SYSTEM_STATE</b></dt>
<dt>L"SystemState"</dt>
</dl>
</td>
<td width="60%">
System State

</td>
</tr>
<tr>
<td width="40%"><a id="SL_INFO_KEY_ACTIVE_PLUGINS"></a><a id="sl_info_key_active_plugins"></a><dl>
<dt><b>SL_INFO_KEY_ACTIVE_PLUGINS</b></dt>
<dt>L"ActivePlugins" </dt>
</dl>
</td>
<td width="60%">
Fully-qualified DLL paths for all active plugins         
				(<b>NULL</b> delimited and double <b>NULL</b>-terminated)

</td>
</tr>
<tr>
<td width="40%"><a id="SL_INFO_KEY_SECURE_STORE_ID"></a><a id="sl_info_key_secure_store_id"></a><dl>
<dt><b>SL_INFO_KEY_SECURE_STORE_ID</b></dt>
<dt>L"SecureStoreId"</dt>
</dl>
</td>
<td width="60%">
Secure store ID (GUID)

</td>
</tr>
<tr>
<td width="40%"><a id="SL_INFO_KEY_SESSION_MACHINE_ID"></a><a id="sl_info_key_session_machine_id"></a><dl>
<dt><b>SL_INFO_KEY_SESSION_MACHINE_ID</b></dt>
<dt>L"SessionMachineId"</dt>
</dl>
</td>
<td width="60%">
Session machine ID (Binary BLOB)

</td>
</tr>
</table>
 


### -param peDataType [out, optional]

Type: <b><a href="https://msdn.microsoft.com/245e79de-4823-4af9-926a-088e263cc802">SLDATATYPE</a>*</b>

A pointer to a value of the <a href="https://msdn.microsoft.com/245e79de-4823-4af9-926a-088e263cc802">SLDATATYPE</a> enumeration that specifies the type of data in the <i>ppbValue</i> buffer.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SL_DATA_SZ"></a><a id="sl_data_sz"></a><dl>
<dt><b>SL_DATA_SZ</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
<b>UNICODE</b> string

</td>
</tr>
<tr>
<td width="40%"><a id="SL_DATA_DWORD"></a><a id="sl_data_dword"></a><dl>
<dt><b>SL_DATA_DWORD</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
<b>DWORD</b>

</td>
</tr>
<tr>
<td width="40%"><a id="SL_DATA_BINARY"></a><a id="sl_data_binary"></a><dl>
<dt><b>SL_DATA_BINARY</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Binary blob

</td>
</tr>
<tr>
<td width="40%"><a id="SL_DATA_MULTI_SZ"></a><a id="sl_data_multi_sz"></a><dl>
<dt><b>SL_DATA_MULTI_SZ</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Double null-terminated <b>UNICODE</b> string array

</td>
</tr>
</table>
 


### -param pcbValue [out]

Type: <b>UINT*</b>

A pointer to the size, in bytes, of the <i>ppbValue</i> buffer.


### -param ppbValue [out]

Type: <b>PBYTE*</b>

If successful, the data is returned in the buffer allocated by SLC.    
		When finished using the memory, free it by calling the <a href="https://msdn.microsoft.com/a0393983-cb43-4dfa-91a6-d82a5fb8de12">LocalFree</a> function.


## -returns



Type: <b>HRESULT WINAPI</b>

If this function succeeds, it return <b>S_OK</b>.  Otherwise, it returns an <b>HRESULT</b> error code.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
<dt>0x80070057</dt>
</dl>
</td>
<td width="60%">
One or more arguments are not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SL_E_VALUE_NOT_FOUND</b></dt>
<dt>0xC004F012</dt>
</dl>
</td>
<td width="60%">
The value for the input key was not found.

</td>
</tr>
</table>
 



