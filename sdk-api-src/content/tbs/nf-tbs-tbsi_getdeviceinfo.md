---
UID: NF:tbs.Tbsi_GetDeviceInfo
title: Tbsi_GetDeviceInfo function (tbs.h)
description: Obtains the version of the TPM on the computer.
helpviewer_keywords: ["Tbsi_GetDeviceInfo","Tbsi_GetDeviceInfo function [TBS]","tbs.tbsi_getdeviceinfo","tbs/Tbsi_GetDeviceInfo"]
old-location: tbs\tbsi_getdeviceinfo.htm
tech.root: TBS
ms.assetid: 49C36A54-0D21-461C-A240-8D12ADF2AFA1
ms.date: 12/05/2018
ms.keywords: Tbsi_GetDeviceInfo, Tbsi_GetDeviceInfo function [TBS], tbs.tbsi_getdeviceinfo, tbs/Tbsi_GetDeviceInfo
req.header: tbs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Tbs.lib
req.dll: Tbs.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - Tbsi_GetDeviceInfo
 - tbs/Tbsi_GetDeviceInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Tbs.dll
api_name:
 - Tbsi_GetDeviceInfo
---

# Tbsi_GetDeviceInfo function


## -description

Obtains the version of the TPM on the computer.

## -parameters

### -param Size [in]

Size of the memory location.

### -param Info [out]

A pointer to a <a href="/windows/desktop/api/tbs/ns-tbs-tpm_device_info">TPM_DEVICE_INFO</a> structure is returned containing the version information about the TPM. The location must be large enough to hold four 32-bit values.

## -returns

If the function succeeds, the function returns TBS_SUCCESS.

If the function fails, it returns a TBS return code that indicates the error.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TBS_SUCCESS</b></dt>
<dt>0 (0x0)</dt>
</dl>
</td>
<td width="60%">
The function was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TBS_E_BAD_PARAMETER</b></dt>
<dt>2150121474 (0x80284002)</dt>
</dl>
</td>
<td width="60%">
One or more parameter values are not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TBS_E_TPM_NOT_FOUND</b></dt>
<dt>2150121487 (0x8028400F)</dt>
</dl>
</td>
<td width="60%">
A compatible Trusted Platform Module (TPM) Security Device cannot be found on this computer.

</td>
</tr>
</table>