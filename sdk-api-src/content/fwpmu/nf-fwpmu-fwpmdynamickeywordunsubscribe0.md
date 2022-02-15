---
UID: NF:fwpmu.FwpmDynamicKeywordUnsubscribe0
title: FwpmDynamicKeywordUnsubscribe0
description: Cancels the delivery of notifications regarding changes to particular dynamic keyword address ([FW_DYNAMIC_KEYWORD_ADDRESS0](/windows/win32/api/netfw/ns-netfw-fw_dynamic_keyword_address0)) objects.
tech.root: fwp
ms.date: 05/17/2021
req.construct-type: function
req.header: fwpmu.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Fwpuclnt.lib
req.dll: Fwpuclnt.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
f1_keywords:
 - FwpmDynamicKeywordUnsubscribe0
 - fwpmu/FwpmDynamicKeywordUnsubscribe0
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Fwpuclnt.dll
api_name:
 - FwpmDynamicKeywordUnsubscribe0
---

## -description

Cancels the delivery of notifications regarding changes to particular dynamic keyword address ([FW_DYNAMIC_KEYWORD_ADDRESS0](/windows/win32/api/netfw/ns-netfw-fw_dynamic_keyword_address0)) objects.

For more info, and code examples, see [Firewall dynamic keywords](/windows/win32/ics/firewall-dynamic-keywords).

## -parameters

### -param subscriptionHandle

Type: \_In\_ **[HANDLE](/windows/win32/winprog/windows-data-types)**

The subscription handle that was returned from [FwpmDynamicKeywordSubscribe0](nf-fwpmu-fwpmdynamickeywordsubscribe0.md).

## -returns

Type: **[DWORD](/windows/win32/winprog/windows-data-types)**

If the function succeeds, then it returns **ERROR_SUCCESS**.

## -remarks

**FwpmDynamicKeywordUnsubscribe0** waits for all callback functions to complete before returning.

## -see-also

* [Firewall dynamic keywords](/windows/win32/ics/firewall-dynamic-keywords)
* [FW_DYNAMIC_KEYWORD_ADDRESS0](/windows/win32/api/netfw/ns-netfw-fw_dynamic_keyword_address0)
