---
UID: NF:sysinfoapi.IsUserCetAvailableInEnvironment
title: IsUserCetAvailableInEnvironment
ms.date: 4/28/2020
targetos: Windows
description: Queries whether user-mode Hardware-enforced Stack Protection is available for the specified environment.
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: sysinfoapi.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
api_location:
 - api-ms-win-core-sysinfo-l1-2-7.dll
 - api-ms-win-core-sysinfo-l1-2-6.dll
 - sysinfoapi.h
api_name:
 - IsUserCetAvailableInEnvironment
f1_keywords:
 - IsUserCetAvailableInEnvironment
 - sysinfoapi/IsUserCetAvailableInEnvironment
dev_langs:
 - c++
---

## -description

Queries whether user-mode Hardware-enforced Stack Protection is available for the specified environment.

## -parameters

### -param UserCetEnvironment

The environment to query. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="USER_CET_ENVIRONMENT_WIN32_PROCESS"></a><a id="user_cet_environment_win32_process"></a><dl>
<dt><b>USER_CET_ENVIRONMENT_WIN32_PROCESS</b></dt>
<dt>0x00000000UL</dt>
</dl>
</td>
<td width="60%">
The Win32 environment.

</td>
</tr>
<tr>
<td width="40%"><a id="USER_CET_ENVIRONMENT_SGX2_ENCLAVE"></a><a id="user_cet_environment_sgx2_enclave"></a><dl>
<dt><b>USER_CET_ENVIRONMENT_SGX2_ENCLAVE</b></dt>
<dt>0x00000002UL</dt>
</dl>
</td>
<td width="60%">
The Intel Software Guard Extensions 2 (SGX2) enclave environment.

</td>
</tr>
<tr>
<td width="40%"><a id="USER_CET_ENVIRONMENT_VBS_ENCLAVE"></a><a id="user_cet_environment_vbs_enclave"></a><dl>
<dt><b>USER_CET_ENVIRONMENT_VBS_ENCLAVE</b></dt>
<dt>0x00000010UL</dt>
</dl>
</td>
<td width="60%">
The virtualization-based security (VBS) enclave environment.

</td>
</tr>
<tr>
<td width="40%"><a id="USER_CET_ENVIRONMENT_VBS_BASIC_ENCLAVE"></a><a id="user_cet_environment_vbs_basic_enclave"></a><dl>
<dt><b>USER_CET_ENVIRONMENT_VBS_BASIC_ENCLAVE</b></dt>
<dt>0x00000011UL</dt>
</dl>
</td>
<td width="60%">
The virtualization-based security (VBS) basic enclave environment.

</td>
</tr>
</table>

## -returns

TRUE if user-mode Hardware-enforced Stack Protection is available for the specified environment, FALSE otherwise.

## -remarks

## -see-also

