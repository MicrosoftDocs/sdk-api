---
UID: NF:mi.MI_Context_Canceled
title: MI_Context_Canceled function
author: windows-sdk-content
description: Determines whether the operation has been canceled. This function is reserved; instead, use the MI_Context_RegisterCancel function.
old-location: wmi_v2\mi_context_canceled.htm
tech.root: wmi_v2
ms.assetid: d8050079-978d-461b-8cf7-e6a08e4d026f
ms.author: windowssdkdev
ms.date: 08/13/2018
ms.keywords: MI_Context_Canceled, MI_Context_Canceled function [Windows Management Infrastructure (MI)], mi/MI_Context_Canceled, wmi.mi_canceled, wmi_v2.mi_context_canceled
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
 - MI_Context_Canceled
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
---

# MI_Context_Canceled function


## -description


Determines whether the operation has been canceled. This function is reserved; instead, use the <a href="https://msdn.microsoft.com/7e6b2016-6ce5-4dcd-b5f4-6e6d24c46f0a">MI_Context_RegisterCancel</a> function.


## -parameters




### -param context [in]

A pointer to the request context that was passed to the provider method.


### -param flag [out]

A pointer to a flag that holds the deletion result. Upon return, this flag will be <b>MI_TRUE</b> if the operation has been successfully canceled; 
     otherwise, it will be <b>MI_FALSE</b>.


## -returns



This function returns MI_INLINE MI_Result MI_INLINE_CALL.




## -remarks



A canceled operation on the client does not always signal to the server that the operation should be canceled. It depends on both the type of operation and the support from the underlying protocol handler.



