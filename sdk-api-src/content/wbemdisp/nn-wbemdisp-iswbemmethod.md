---
UID: NN:wbemdisp.ISWbemMethod
title: ISWbemMethod
author: windows-sdk-content
description: You can use the properties of the SWbemMethod object to inspect a single method definition of a WMI object. This object cannot be created by the VBScript CreateObject call.
old-location: wmi\swbemmethod.htm
old-project: WmiSdk
ms.assetid: 461d5c41-4930-40cf-96e2-bc8cae335b60
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: ISWbemMethod, SWbemMethod, SWbemMethod object [Windows Management Instrumentation], SWbemMethod object [Windows Management Instrumentation],described, _hmm_swbemmethod, wbemdisp/SWbemMethod, wmi.swbemmethod
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: wbemdisp.h
req.include-header: 
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
 - SWbemMethod
 - ISWbemMethod
product: Windows
targetos: Windows
req.lib: 
req.dll: Wbemdisp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISWbemMethod interface


## -description


You can use the properties of the 
<b>SWbemMethod</b> object to inspect a single method definition of a WMI object. This object cannot be created by the VBScript <b>CreateObject</b> call.

This object can be used to inspect the definitions of methods. To invoke the methods, you should use either direct access (see 
<a href="https://msdn.microsoft.com/682cbe12-1487-4681-8d2f-4caf21cb068a">Manipulating Class and Instance Information</a>) on an 
<a href="https://msdn.microsoft.com/d303ec1a-5e0c-4a5e-8ed3-ed353a138755">SWbemObject</a> (which is the recommended mechanism) object, or the 
<a href="https://msdn.microsoft.com/2637efdc-fde5-4a44-a41f-67e0fb0df19d">SWbemServices.ExecMethod</a> call.
<div class="alert"><b>Note</b>  In this version of the API, write access to method information is not supported. If you want to define methods or modify existing method definitions, you can define the method changes in a MOF file and submit the changes using the 
<a href="https://msdn.microsoft.com/8c107611-36f8-4657-8b54-dbf54b3dfb7b">MOF Compiler</a>. Alternatively, use the 
<a href="https://msdn.microsoft.com/5fa8f1b5-fd19-4d45-9b53-bc7089eecdb1">COM API for WMI</a>.</div><div> </div>

## -see-also




<a href="https://msdn.microsoft.com/91bc0fad-1a4b-4b48-b5a0-1a6502d2ab26">Scripting API Objects</a>
 

 

