---
UID: NS:winnt._PROCESS_MITIGATION_FONT_DISABLE_POLICY
title: PROCESS_MITIGATION_FONT_DISABLE_POLICY (winnt.h)
description: Contains process mitigation policy settings for the loading of non-system fonts.
helpviewer_keywords: ["*PPROCESS_MITIGATION_FONT_DISABLE_POLICY","PPROCESS_MITIGATION_FONT_DISABLE_POLICY","PPROCESS_MITIGATION_FONT_DISABLE_POLICY structure pointer","PROCESS_MITIGATION_FONT_DISABLE_POLICY","PROCESS_MITIGATION_FONT_DISABLE_POLICY structure","base.process_mitigation_font_disable_policy","winnt/PPROCESS_MITIGATION_FONT_DISABLE_POLICY","winnt/PROCESS_MITIGATION_FONT_DISABLE_POLICY"]
old-location: base\process_mitigation_font_disable_policy.htm
tech.root: backup
ms.assetid: 7DDBEDEC-55F4-4DEA-8FFD-EA128FAA1A9B
ms.date: 12/05/2018
ms.keywords: '*PPROCESS_MITIGATION_FONT_DISABLE_POLICY, PPROCESS_MITIGATION_FONT_DISABLE_POLICY, PPROCESS_MITIGATION_FONT_DISABLE_POLICY structure pointer, PROCESS_MITIGATION_FONT_DISABLE_POLICY, PROCESS_MITIGATION_FONT_DISABLE_POLICY structure, base.process_mitigation_font_disable_policy, winnt/PPROCESS_MITIGATION_FONT_DISABLE_POLICY, winnt/PROCESS_MITIGATION_FONT_DISABLE_POLICY'
req.header: winnt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
req.typenames: PROCESS_MITIGATION_FONT_DISABLE_POLICY, *PPROCESS_MITIGATION_FONT_DISABLE_POLICY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PROCESS_MITIGATION_FONT_DISABLE_POLICY
 - winnt/_PROCESS_MITIGATION_FONT_DISABLE_POLICY
 - PPROCESS_MITIGATION_FONT_DISABLE_POLICY
 - winnt/PPROCESS_MITIGATION_FONT_DISABLE_POLICY
 - PROCESS_MITIGATION_FONT_DISABLE_POLICY
 - winnt/PROCESS_MITIGATION_FONT_DISABLE_POLICY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinNT.h
api_name:
 - PROCESS_MITIGATION_FONT_DISABLE_POLICY
---

# PROCESS_MITIGATION_FONT_DISABLE_POLICY structure


## -description

Contains process mitigation policy settings for the loading of non-system fonts.

## -struct-fields

### -field DUMMYUNIONNAME

### -field DUMMYUNIONNAME.Flags

Reserved for system use.

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.DisableNonSystemFonts

Set (0x1) to prevent the process from loading non-system fonts;  otherwise leave unset (0x0).

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.AuditNonSystemFontLoading

Set (0x1) to indicate that an Event Tracing for Windows (ETW) event should be logged when the process attempts to load a non-system font; leave unset (0x0) to indicate that an ETW event should not be logged.

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.ReservedFlags

Reserved for system use.

## -see-also

<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getprocessmitigationpolicy">GetProcessMitigationPolicy</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setprocessmitigationpolicy">SetProcessMitigationPolicy</a>