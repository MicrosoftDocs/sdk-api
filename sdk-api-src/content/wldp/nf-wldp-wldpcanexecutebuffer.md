---
UID: NF:wldp.WldpCanExecuteBuffer
tech.root: security
title: WldpCanExecuteBuffer
ms.date: 08/23/2022
targetos: Windows
description: Queries whether the execution policy allows execution of the code in the supplied buffer.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: wldp.dll
req.header: wldp.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: wldp.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 11, Build 22621
req.target-min-winversvr: Windows 11, Build 22621
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - wldp.dll
api_name:
 - WldpCanExecuteBuffer
f1_keywords:
 - WldpCanExecuteBuffer
 - wldp/WldpCanExecuteBuffer
dev_langs:
 - c++
helpviewer_keywords:
 - WldpCanExecuteBuffer
---

## -description

Queries whether the execution policy allows execution of the code in the supplied buffer.

## -parameters

### -param host [in]

A GUID specifying the calling program. For the list of pre-defined GUIDs that can be used for this parameter, see [WLDP Host GUIDs](/windows/win32/devnotes/wldp-host-guids). For hosts for which a specific value is not defined, use GUID WLDP_HOST_GUID_OTHER.

### -param options [in]

A value from the [WLDP_EXECUTION_EVALUATION_OPTIONS](ne-wldp-wldp_execution_evaluation_options.md) specifying options for the execution authorization request.

### -param buffer [in]

The buffer containing script code to be validated. 

> [!IMPORTANT]
> Buffers passed to **WldpCanExecuteBuffer** should be read-only and the caller should not cache the security authorization on a specific buffer. These measures are necessary to prevent [TOC/TOU vulnerabilities](https://en.wikipedia.org/wiki/Time-of-check_to_time-of-use) that could subvert script enforcement policy.

### -param bufferSize [in]

The size of *buffer*, in bytes.

### -param auditInfo [in, optional]

A string that should include relevant contextual information for the caller to use in debugging. If an authorization request fails this string will be recorded in the event log, under “Applocker/MSI and Scripts/Operational”. Callers should note that, while the *AuditInfo* is not size limited, the string should be less than 4K bytes in size because it will be placed in the event log. 

### -param result [out]

Receives a pointer to a value from the [WLDP_EXECUTION_POLICY](ne-wldp-wldp_execution_policy.md) enumeration, indicating the execution policy result of the query.

## -returns

Returns S_OK on success and a failure code otherwise.

## -remarks

This method is provided as a replacement for [WldpGetLockdownPolicy](nf-wldp-wldpgetlockdownpolicy.md). This interface is differentiated from **WldpGetLockdownPolicy** in the following ways:

- Encourages callers to ensure that the subject (file, buffer, or stream) passes os execution policy.  
- Allows calling apps to provide additional audit information for diagnostic purposes.
- Allows verification of buffers and streams of code.
- Simplifies the calling pattern. 
- Supports fine grained execution policies like for example interactive mode in cmd or powershell


## -see-also

- [WldpCanExecuteFile](nf-wldp-wldpcanexecutefile.md)
- [WldpCanExecuteStream](nf-wldp-wldpcanexecutestream.md)

