---
UID: NF:objidlbase.IPipeByte.Push
title: IPipeByte::Push
author: windows-sdk-content
description: Sends data of the byte type to the pipe source.
old-location: com\ipipebyte_push.htm
old-project: com
ms.assetid: 7dd672d3-22ef-4786-85e0-d5c2ebabaea2
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: IPipeByte interface [COM],Push method, IPipeByte.Push, IPipeByte::Push, Push, Push method [COM], Push method [COM],IPipeByte interface, _com_ipipebyte_push, com.ipipebyte_push, objidlbase/IPipeByte::Push
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: objidlbase.h
req.include-header: ObjIdl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: THDTYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - objidlbase.h
api_name:
 - IPipeByte.Push
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IPipeByte::Push


## -description


Sends data of the byte type to the pipe source.


## -parameters




### -param buf [in]

A pointer to the memory buffer that holds the data to be sent.


### -param cSent [in]

The number of bytes in the buffer.


## -returns



This method returns S_OK to indicate that the data was sent successfully.




## -remarks



When the <b>Push</b> method is called, the data is being sent to the provider of the pipe. The caller fills the buffer with the data and then calls <b>Push</b>. The number of bytes being sent is specified in the <i>cSent</i> parameter. The caller is responsible for ensuring that the buffer is valid for the duration of the call.

When the last of the data has been pushed, the caller must do one last push of <i>cSent</i> equal to 0 to indicate that the data transfer is complete.




## -see-also




<a href="https://msdn.microsoft.com/e3e01280-c015-488a-8be4-9740c44c0041">IPipeByte</a>
 

 

