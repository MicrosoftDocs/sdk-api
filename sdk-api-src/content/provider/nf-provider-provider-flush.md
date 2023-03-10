---
UID: NF:provider.Provider.Flush
title: Provider::Flush (provider.h)
description: The Flush method is called by the provider framework to delete all unnecessary memory in use by the provider.
helpviewer_keywords: ["?Flush@Provider@@MAEXXZ","?Flush@Provider@@MEAAXXZ","Flush","Flush method [Windows Management Instrumentation]","Flush method [Windows Management Instrumentation]","Provider interface","Provider interface [Windows Management Instrumentation]","Flush method","Provider.Flush","Provider::Flush","_hmm_provider_flush","provider/Provider::Flush","wmi.provider_flush"]
old-location: wmi\provider_flush.htm
tech.root: wmi
ms.assetid: c8be35ec-cd2e-45ec-b47f-48acf5e6f51a
ms.date: 12/05/2018
ms.keywords: ?Flush@Provider@@MAEXXZ, ?Flush@Provider@@MEAAXXZ, Flush, Flush method [Windows Management Instrumentation], Flush method [Windows Management Instrumentation],Provider interface, Provider interface [Windows Management Instrumentation],Flush method, Provider.Flush, Provider::Flush, _hmm_provider_flush, provider/Provider::Flush, wmi.provider_flush
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
req.lib: FrameDyn.lib
req.dll: FrameDynOS.dll; FrameDyn.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - Provider::Flush
 - provider/Provider::Flush
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - FrameDynOS.dll
 - FrameDyn.dll
api_name:
 - Provider.Flush
 - ?Flush@Provider@@MAEXXZ
 - ?Flush@Provider@@MEAAXXZ
---

# Provider::Flush


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/provider/nl-provider-provider">Provider</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>Flush</b> method is called by the provider framework to delete all unnecessary memory in use by the provider. Because your provider may be called again after a call to <b>Flush</b>, you must re-create any objects released by <b>Flush</b>. If you override this method, you should call the parent object's <b>Flush</b> method to release any framework memory associated with your provider.



## -remarks

Override this method only if your framework provider allocates memory that can be flushed. If your provider chooses to override, include a call to <b>Provider::Flush</b> in the provider's implementation.

<div class="alert"><b>Note</b>  Because your provider may be called after a call to <b>Flush</b>, you must be prepared to re-create any items released by the call to <b>Flush</b>.</div>
<div> </div>
