---
UID: NE:wbemdisp.WbemTimeout
title: WbemTimeout
author: windows-sdk-content
description: Defines the time-out constants. This constant is used by SWbemEventSource.NextEvent.
old-location: wmi\wbemtimeout.htm
old-project: WmiSdk
ms.assetid: 1dfe8412-0b6a-40be-94b7-c993851a9205
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: WbemTimeout, WbemTimeout enumeration [Windows Management Instrumentation], _hmm_wbemtimeout, wbemTimeoutInfinite, wbemdisp/WbemTimeout, wbemdisp/wbemTimeoutInfinite, wmi.wbemtimeout
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: wbemdisp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wbemdisp.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WbemTimeout
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wbemdisp.h
api_name:
 - WbemTimeout
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# WbemTimeout enumeration


## -description


The 
WbemTimeout constant defines the time-out constants. This constant is used by 
<a href="https://msdn.microsoft.com/ff2d54d4-b8ee-4bb8-b6f7-081a1ca20489">SWbemEventSource.NextEvent</a>.

The WMI scripting type library, wbemdisp.tlb, defines these constants. Visual Basic applications can access this library; script languages must use the value of the constant directly, unless they use Windows Script Host (WSH) XML file format. For more information, see 
<a href="https://msdn.microsoft.com/6ef4e210-0733-4f2a-89c1-1a7aca5a19d9">Using the WMI Scripting Type Library</a>.


## -enum-fields




### -field wbemTimeoutInfinite

Use for parameters that use a time-out value such as <i>iTimeoutMs</i> for <a href="https://msdn.microsoft.com/fe547660-4095-4a75-829d-f06599c0d9d7">ISWbemServices.ExecNotificationQuery</a> and the call will not return unless an event is received.


## -see-also




<a href="https://msdn.microsoft.com/feaab757-3167-420b-8f42-edced4cd4c53">Scripting API Constants</a>
 

 

