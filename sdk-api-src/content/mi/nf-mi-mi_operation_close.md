---
UID: NF:mi.MI_Operation_Close
title: MI_Operation_Close function (mi.h)
description: Closes an operation handle.
helpviewer_keywords: ["MI_Operation_Close","MI_Operation_Close function [Windows Management Infrastructure (MI)]","mi/MI_Operation_Close","wmi_v2.mi_operation_close"]
old-location: wmi_v2\mi_operation_close.htm
tech.root: wmi_v2
ms.assetid: 3e698e34-d537-4ea4-9345-cc4f493ff823
ms.date: 12/05/2018
ms.keywords: MI_Operation_Close, MI_Operation_Close function [Windows Management Infrastructure (MI)], mi/MI_Operation_Close, wmi_v2.mi_operation_close
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
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1,     Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
f1_keywords:
 - MI_Operation_Close
 - mi/MI_Operation_Close
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mi.h
api_name:
 - MI_Operation_Close
---

# MI_Operation_Close function


## -description

Closes an operation handle.

## -parameters

### -param operation [in, out]

A pointer to an operation handle that was returned from a call to one of the 
      <a href="/windows/desktop/api/mi/ns-mi-mi_session">MI_Session</a> operation functions. For asynchronous 
      callbacks, it can also be the operation handle that is passed into the callback.

## -returns

A value of the <a href="/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the 
      function return code. This can be one of the following codes.

## -remarks

For synchronous operations, the close function is synchronous on retrieving the final result, so if the client 
     does not retrieve all results, then this call will fail. For asynchronous operations, this function will not 
     block.

A closing operation, such as <b>MI_Operations_Close</b>, should be called in same security 
     context as the starting operation.