---
UID: NF:mi.MI_Operation_Close
title: MI_Operation_Close function
author: windows-sdk-content
description: Closes an operation handle.
old-location: wmi_v2\mi_operation_close.htm
old-project: wmi_v2
ms.assetid: 3e698e34-d537-4ea4-9345-cc4f493ff823
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: MI_Operation_Close, MI_Operation_Close function [Windows Management Infrastructure (MI)], mi/MI_Operation_Close, wmi_v2.mi_operation_close
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: mi.h
req.include-header: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1,     Windows 7 with SP1, and Windows Server 2008 with SP2
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
tech.root: 
req.typenames: MI_Type
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mi.h
api_name:
 - MI_Operation_Close
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MI_Operation_Close function


## -description


Closes an operation handle.


## -parameters




### -param operation [in, out]

A pointer to an operation handle that was returned from a call to one of the 
      <a href="https://msdn.microsoft.com/68a69321-0aa9-423e-a72f-aa2f4dee2d51">MI_Session</a> operation functions. For asynchronous 
      callbacks, it can also be the operation handle that is passed into the callback.


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the 
      function return code. This can be one of the following codes.




## -remarks



For synchronous operations, the close function is synchronous on retrieving the final result, so if the client 
     does not retrieve all results, then this call will fail. For asynchronous operations, this function will not 
     block.

A closing operation, such as <b>MI_Operations_Close</b>, should be called in same security 
     context as the starting operation.



