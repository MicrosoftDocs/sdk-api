---
UID: NF:wbemdisp.ISWbemDateTime.put_UTC
title: ISWbemDateTime::put_UTC
author: windows-sdk-content
description: Gets or sets the Coordinated Universal Times (UTC) representation of the datetime value.
old-location: wmi\swbemdatetime_utc.htm
old-project: WmiSdk
ms.assetid: 43d9d0c8-5521-410f-825b-6b00c3dd0039
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: ISWbemDateTime interface [Windows Management Instrumentation],UTC property, ISWbemDateTime.get_UTC, ISWbemDateTime.put_UTC, ISWbemDateTime::put_UTC, SWbemDateTime object [Windows Management Instrumentation],UTC property, SWbemDateTime.UTC, UTC property [Windows Management Instrumentation], UTC property [Windows Management Instrumentation],ISWbemDateTime interface, UTC property [Windows Management Instrumentation],SWbemDateTime object, _hmm_swbemdatetime.utc, put_UTC, wmi.swbemdatetime_utc
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wbemdisp.h
req.include-header: 
req.redist: 
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
req.type-library: Wbemdisp.tlb
tech.root: 
req.typenames: WbemTimeout
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wbemdisp.dll
api_name:
 - SWbemDateTime.UTC
 - ISWbemDateTime.UTC
 - ISWbemDateTime.get_UTC
 - ISWbemDateTime.put_UTC
product: Windows
targetos: Windows
req.lib: 
req.dll: Wbemdisp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISWbemDateTime::put_UTC


## -description


The 
<b>UTC</b> property of the 
<a href="https://msdn.microsoft.com/3dd34c73-3c2b-4d59-827b-169cf8020213">SWbemDateTime</a> object gets or sets the Coordinated Universal Times (UTC) representation of the <b>datetime</b> value. UTC is the time as set by the World Time Standard. UTC has replaced Greenwich Mean Time (GMT). A UTC value with a zero offset is the same as GMT with a zero offset. The signed number must be in the range of -720 through 720 or the error <b>wbemErrValueOutOfRange</b> is returned.

For an explanation of this syntax, see 
<a href="https://msdn.microsoft.com/889e6322-96f6-4a24-a084-e3b7bfa94a40">Document Conventions for the Scripting API</a>.

This property is read/write.


## -parameters


## -see-also




<a href="https://msdn.microsoft.com/2c18ef4d-4eb6-4c73-ad2e-31995b79e99d">DATETIME</a>



<a href="https://msdn.microsoft.com/3dd34c73-3c2b-4d59-827b-169cf8020213">SWbemDateTime</a>



<a href="https://msdn.microsoft.com/9cb04351-294b-48ba-8d1c-2f28cb9ce463">SWbemDateTime.UTCSpecified</a>
 

 

