---
UID: NC:fwpmu.FWPM_DYNAMIC_KEYWORD_CALLBACK0
title: FWPM_DYNAMIC_KEYWORD_CALLBACK0
description: A callback function, which you implement, that is invoked with notifications regarding changes to dynamic keyword address ([FW_DYNAMIC_KEYWORD_ADDRESS0](/windows/win32/api/netfw/ns-netfw-fw_dynamic_keyword_address0)) objects.
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
f1_keywords:
 - FWPM_DYNAMIC_KEYWORD_CALLBACK0
 - fwpmu/FWPM_DYNAMIC_KEYWORD_CALLBACK0
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - fwpmu.h
api_name:
 - FWPM_DYNAMIC_KEYWORD_CALLBACK0
---

## -description

A callback function, which you implement, that is invoked with notifications regarding changes to dynamic keyword address ([FW_DYNAMIC_KEYWORD_ADDRESS0](/windows/win32/api/netfw/ns-netfw-fw_dynamic_keyword_address0)) objects. See [FwpmDynamicKeywordSubscribe0](nf-fwpmu-fwpmdynamickeywordsubscribe0.md).

For more info, and code examples, see [Firewall dynamic keywords](/windows/win32/ics/firewall-dynamic-keywords).

## -parameters

### -param notification

Type: \_In\_opt\_ **void\***

Not used.

### -param context

Type: \_In\_opt\_ **void\***

The value you pass to [FwpmDynamicKeywordSubscribe0](nf-fwpmu-fwpmdynamickeywordsubscribe0.md) as the *context* argument.

## -remarks

## -see-also

* [Firewall dynamic keywords](/windows/win32/ics/firewall-dynamic-keywords)
* [FwpmDynamicKeywordSubscribe0](nf-fwpmu-fwpmdynamickeywordsubscribe0.md)
* [FW_DYNAMIC_KEYWORD_ADDRESS0](/windows/win32/api/netfw/ns-netfw-fw_dynamic_keyword_address0)
