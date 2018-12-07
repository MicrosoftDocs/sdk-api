---
UID: NF:mi.MI_Context_WriteCimError
title: MI_Context_WriteCimError function
author: windows-sdk-content
description: Sends a CIM (informative) error instance to the client.
old-location: wmi_v2\mi_context_writecimerror.htm
tech.root: wmi_v2
ms.assetid: 6df0841b-3e13-4f9a-9e54-5c3c0c0d79fe
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: MI_Context_WriteCimError, MI_Context_WriteCimError function [Windows Management Infrastructure (MI)], mi/MI_Context_WriteCimError, wmi.mi_writecimerror, wmi_v2.mi_context_writecimerror
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
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
 - Mi.h
api_name:
 - MI_Context_WriteCimError
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
---

# MI_Context_WriteCimError function


## -description


Sends a CIM (informative) error instance to the client.


## -parameters




### -param context [in]

Request context.


### -param error [in]

An instance of a <a href="https://msdn.microsoft.com/e57636aa-6e04-4159-8fe1-5cc14d193891">CIM_Error</a> class.


### -param flag [out]

<b>MI_TRUE</b> on return if the provider should continue execution. Otherwise, <b>MI_FALSE</b>.


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.




## -remarks



A provider calls this function to send a CIM error instance to the client.  This does not cancel the operation. Rather, this indicates the error to the client and gives the client the opportunity to determine if the operation should be continued or cancelled. It is then up to the provider to react accordingly.




## -see-also




<a href="https://msdn.microsoft.com/e57636aa-6e04-4159-8fe1-5cc14d193891">CIM_Error</a>



<a href="https://msdn.microsoft.com/51d6c510-f9fd-4ab7-a669-b2a5776b496d">MI_Context</a>



<a href="https://msdn.microsoft.com/96ef9e97-467b-4b71-a7f9-4f640102e744">MI_Context_PostCimError</a>



<a href="https://msdn.microsoft.com/3dce1817-7995-49e5-8cc0-ee9496665e5c">MI_Instance</a>
 

 

