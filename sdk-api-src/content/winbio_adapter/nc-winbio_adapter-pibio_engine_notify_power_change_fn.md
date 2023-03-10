---
UID: NC:winbio_adapter.PIBIO_ENGINE_NOTIFY_POWER_CHANGE_FN
title: PIBIO_ENGINE_NOTIFY_POWER_CHANGE_FN (winbio_adapter.h)
description: Receives notification about a change in the computer power state and prepares the engine adapter accordingly.
helpviewer_keywords: ["EngineAdapterNotifyPowerChange","EngineAdapterNotifyPowerChange callback function [Windows Biometric Framework API]","PBT_APMPOWERSTATUSCHANGE","PBT_APMRESUMEAUTOMATIC","PBT_APMSUSPEND","PIBIO_ENGINE_NOTIFY_POWER_CHANGE_FN","PIBIO_ENGINE_NOTIFY_POWER_CHANGE_FN callback","secbiomet.engineadapternotifypowerchange","winbio_adapter/EngineAdapterNotifyPowerChange"]
old-location: secbiomet\engineadapternotifypowerchange.htm
tech.root: SecBioMet
ms.assetid: 805152AE-CCFE-4C05-8142-F9EF8D124625
ms.date: 11/19/2020
ms.keywords: EngineAdapterNotifyPowerChange, EngineAdapterNotifyPowerChange callback function [Windows Biometric Framework API], PBT_APMPOWERSTATUSCHANGE, PBT_APMRESUMEAUTOMATIC, PBT_APMSUSPEND, PIBIO_ENGINE_NOTIFY_POWER_CHANGE_FN, PIBIO_ENGINE_NOTIFY_POWER_CHANGE_FN callback, secbiomet.engineadapternotifypowerchange, winbio_adapter/EngineAdapterNotifyPowerChange
req.header: winbio_adapter.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PIBIO_ENGINE_NOTIFY_POWER_CHANGE_FN
 - winbio_adapter/PIBIO_ENGINE_NOTIFY_POWER_CHANGE_FN
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Winbio_adapter.h
api_name:
 - EngineAdapterNotifyPowerChange
---

# PIBIO_ENGINE_NOTIFY_POWER_CHANGE_FN callback function


## -description

Called by the Windows Biometric Framework when the computer is ready to enter a low-power state or when the computer has been awakened from a low-power state. The purpose of this function is to enable the adapter to respond to transitions in the computer power state.

## -parameters

### -param Pipeline [in, out]

Pointer to the <a href="/windows/desktop/api/winbio_adapter/ns-winbio_adapter-winbio_pipeline">WINBIO_PIPELINE</a> structure associated with the biometric unit performing the operation.

### -param PowerEventType [in]

Indicates the nature of the change. It can be one of the following values:

* **PBT_APMSUSPEND**

The system is entering a low-power state.

* **PBT_APMRESUMEAUTOMATIC** 

The system is returning from a low-power state.

* **PBT_APMPOWERSTATUSCHANGE**

The status of the system's power source is changing (e.g. the system has switched from battery to line power, or the battery is getting low).



## -returns

If the function succeeds, it returns <b>S_OK</b>. If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following table.  For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

When it receives a <a href="/windows/desktop/Power/pbt-apmpowerstatuschange">PBT_APMPOWERSTATUSCHANGE</a> event, the adapter should call the Microsoft Win32<a href="/windows/desktop/api/winbase/nf-winbase-getsystempowerstatus">GetSystemPowerStatus</a> API to determine the new power status.



The biometric framework calls this adapter entry point asynchronously in the context of an arbitrary thread. It is the responsibility of the adapter to synchronize  processing of this call with any other work it may be doing.

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-getsystempowerstatus">GetSystemPowerStatus</a>



<a href="/windows/desktop/Power/pbt-apmpowerstatuschange">PBT_APMPOWERSTATUSCHANGE</a>