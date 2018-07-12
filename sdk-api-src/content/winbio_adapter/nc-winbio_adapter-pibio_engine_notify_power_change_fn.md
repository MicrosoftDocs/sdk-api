---
UID: NC:winbio_adapter.PIBIO_ENGINE_NOTIFY_POWER_CHANGE_FN
title: PIBIO_ENGINE_NOTIFY_POWER_CHANGE_FN
author: windows-sdk-content
description: Receives notification about a change in the computer power state and prepares the engine adapter accordingly.
old-location: secbiomet\engineadapternotifypowerchange.htm
old-project: secbiomet
ms.assetid: 805152AE-CCFE-4C05-8142-F9EF8D124625
ms.author: windowssdkdev
ms.date: 04/25/2018
ms.keywords: EngineAdapterNotifyPowerChange, EngineAdapterNotifyPowerChange callback function [Windows Biometric Framework API], PBT_APMPOWERSTATUSCHANGE, PBT_APMRESUMEAUTOMATIC, PBT_APMSUSPEND, PIBIO_ENGINE_NOTIFY_POWER_CHANGE_FN, PIBIO_ENGINE_NOTIFY_POWER_CHANGE_FN callback, secbiomet.engineadapternotifypowerchange, winbio_adapter/EngineAdapterNotifyPowerChange
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
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
tech.root: 
req.typenames: WINBIO_ASYNC_RESULT, *PWINBIO_ASYNC_RESULT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Winbio_adapter.h
api_name:
 - EngineAdapterNotifyPowerChange
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# PIBIO_ENGINE_NOTIFY_POWER_CHANGE_FN callback function


## -description


Called by the Windows Biometric Framework when the computer is ready to enter a low-power state or when the computer has been awakened from a low-power state. The purpose of this function is to enable the adapter to respond to transitions in the computer power state.


## -parameters




### -param Pipeline [in, out]

Pointer to the <a href="https://msdn.microsoft.com/b5fc2b14-b0b6-4327-a42a-ecae41c3e12a">WINBIO_PIPELINE</a> structure associated with the biometric unit performing the operation.


### -param PowerEventType [in]

Indicates the nature of the change. It can be one of the following values:



##### )



##### )



####### )


## -returns



If the function succeeds, it returns <b>S_OK</b>. If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following table.  For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



When it receives a <a href="https://msdn.microsoft.com/dc56fee3-e0df-4f8e-8a41-92460279280a">PBT_APMPOWERSTATUSCHANGE</a> event, the adapter should call the Microsoft Win32<a href="https://msdn.microsoft.com/6d440ef2-2b9d-4f7a-a445-2420f07f3784">GetSystemPowerStatus</a>API to determine the new power status.



The biometric framework calls this adapter entry point asynchronously in the context of an arbitrary thread. It is the responsibility of the adapter to synchronize  processing of this call with any other work it may be doing.




## -see-also




<a href="https://msdn.microsoft.com/6d440ef2-2b9d-4f7a-a445-2420f07f3784">GetSystemPowerStatus</a>



<a href="https://msdn.microsoft.com/dc56fee3-e0df-4f8e-8a41-92460279280a">PBT_APMPOWERSTATUSCHANGE</a>
 

 

