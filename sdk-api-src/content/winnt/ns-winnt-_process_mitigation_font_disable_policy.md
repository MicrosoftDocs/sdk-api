---
UID: NS:winnt._PROCESS_MITIGATION_FONT_DISABLE_POLICY
title: "_PROCESS_MITIGATION_FONT_DISABLE_POLICY"
author: windows-sdk-content
description: Contains process mitigation policy settings for the loading of non-system fonts.
old-location: base\process_mitigation_font_disable_policy.htm
tech.root: procthread
ms.assetid: 7DDBEDEC-55F4-4DEA-8FFD-EA128FAA1A9B
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: "*PPROCESS_MITIGATION_FONT_DISABLE_POLICY, PPROCESS_MITIGATION_FONT_DISABLE_POLICY, PPROCESS_MITIGATION_FONT_DISABLE_POLICY structure pointer, PROCESS_MITIGATION_FONT_DISABLE_POLICY, PROCESS_MITIGATION_FONT_DISABLE_POLICY structure, _PROCESS_MITIGATION_FONT_DISABLE_POLICY, base.process_mitigation_font_disable_policy, winnt/PPROCESS_MITIGATION_FONT_DISABLE_POLICY, winnt/PROCESS_MITIGATION_FONT_DISABLE_POLICY"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinNT.h
api_name:
 - PROCESS_MITIGATION_FONT_DISABLE_POLICY
product: Windows
targetos: Windows
req.typenames: PROCESS_MITIGATION_FONT_DISABLE_POLICY, *PPROCESS_MITIGATION_FONT_DISABLE_POLICY
req.redist: 
---

# _PROCESS_MITIGATION_FONT_DISABLE_POLICY structure


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




<a href="https://msdn.microsoft.com/89f9c883-6976-4af2-9a8b-c76101d8ed02">GetProcessMitigationPolicy</a>



<a href="https://msdn.microsoft.com/57f364f8-58d7-447a-91c3-51fc1fe1a481">SetProcessMitigationPolicy</a>
 

 

