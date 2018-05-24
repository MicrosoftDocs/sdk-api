---
UID: NF:provider.Provider.ValidateDeletionFlags
title: Provider::ValidateDeletionFlags
author: windows-driver-content
description: The ValidateDeletionFlags method determines whether a set of flags is valid for a delete operation.
old-location: wmi\provider_validatedeletionflags.htm
old-project: WmiSdk
ms.assetid: eaaf49e3-e768-4494-ba0b-dc2c8c35be47
ms.author: windowsdriverdev
ms.date: 4/11/2018
ms.keywords: "?ValidateDeletionFlags@Provider@@MAEJJ@Z, ?ValidateDeletionFlags@Provider@@MEAAJJ@Z, Provider interface [Windows Management Instrumentation],ValidateDeletionFlags method, Provider.ValidateDeletionFlags, Provider::ValidateDeletionFlags, ValidateDeletionFlags, ValidateDeletionFlags method [Windows Management Instrumentation], ValidateDeletionFlags method [Windows Management Instrumentation],Provider interface, _hmm_provider_validatedeletionflags, provider/Provider::ValidateDeletionFlags, wmi.provider_validatedeletionflags"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: provider.h
req.include-header: FwCommon.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PROPVAR_COMPARE_UNIT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	FrameDynOS.dll
-	FrameDyn.dll
api_name:
-	Provider.ValidateDeletionFlags
-	?ValidateDeletionFlags@Provider@@MAEJJ@Z
-	?ValidateDeletionFlags@Provider@@MEAAJJ@Z
product: Windows
targetos: Windows
req.lib: FrameDyn.lib
req.dll: FrameDynOS.dll; FrameDyn.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# Provider::ValidateDeletionFlags


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/library/windows/hardware/hh406455">Provider</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>ValidateDeletionFlags</b> method determines whether a set of flags is valid for a delete operation.


## -parameters




### -param lFlags

Bitmask of flags that are validated.


## -returns



Returns <b>WBEM_S_NO_ERROR</b> if the flags are valid and <b>WBEM_E_UNSUPPORTED_PARAMETER</b> if one or more flags are not valid.




## -remarks



At present, the <a href="https://msdn.microsoft.com/library/windows/hardware/hh406455">Provider</a> class does not support any deletion flags. Therefore, if <i>lFlags</i> is set to a value other than zero (0),  <b>Provider::ValidateDeletionFlags</b> automatically returns <b>WBEM_E_UNSUPPORTED_PARAMETER</b>.

Framework providers must override this method to validate flags that are unknown to the base <a href="https://msdn.microsoft.com/library/windows/hardware/hh406455">Provider</a> class.



