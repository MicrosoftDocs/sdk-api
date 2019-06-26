---
UID: NE:wbemdisp.WbemTimeout
title: WbemTimeout (wbemdisp.h)
author: windows-sdk-content
description: Defines the time-out constants. This constant is used by SWbemEventSource.NextEvent.
old-location: wmi\wbemtimeout.htm
tech.root: WmiSdk
ms.assetid: 1dfe8412-0b6a-40be-94b7-c993851a9205
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WbemTimeout, WbemTimeout enumeration [Windows Management Instrumentation], _hmm_wbemtimeout, wbemTimeoutInfinite, wbemdisp/WbemTimeout, wbemdisp/wbemTimeoutInfinite, wmi.wbemtimeout
ms.topic: enum
f1_keywords: 
 - "wbemdisp/WbemTimeout"
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
req.lib: 
req.dll: 
req.irql: 
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
req.typenames: WbemTimeout
req.redist: 
ms.custom: 19H1
---

# WbemTimeout enumeration


## -description


The 
WbemTimeout constant defines the time-out constants. This constant is used by 
<a href="https://docs.microsoft.com/windows/desktop/WmiSdk/swbemeventsource-nextevent">SWbemEventSource.NextEvent</a>.

The WMI scripting type library, wbemdisp.tlb, defines these constants. Visual Basic applications can access this library; script languages must use the value of the constant directly, unless they use Windows Script Host (WSH) XML file format. For more information, see 
<a href="https://docs.microsoft.com/windows/desktop/WmiSdk/using-the-wmi-scripting-type-library">Using the WMI Scripting Type Library</a>.


## -enum-fields




### -field wbemTimeoutInfinite

Use for parameters that use a time-out value such as <i>iTimeoutMs</i> for <a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execnotificationquery">ISWbemServices.ExecNotificationQuery</a> and the call will not return unless an event is received.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WmiSdk/scripting-api-constants">Scripting API Constants</a>
 

 

