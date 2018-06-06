---
UID: NS:callobj.__MIDL_ICallFrame_0004
title: "__MIDL_ICallFrame_0004"
author: windows-sdk-content
description: Provides information about the context in which marshalling should be carried out.
old-location: com\callframe_marshalcontext.htm
old-project: com
ms.assetid: 4ecc4646-db3f-4d0e-9c45-b78a288156e1
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: CALLFRAME_MARSHALCONTEXT, CALLFRAME_MARSHALCONTEXT structure [COM], __MIDL_ICallFrame_0004, callobj/CALLFRAME_MARSHALCONTEXT, com.callframe_marshalcontext
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: callobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Callobj.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: CALLFRAME_MARSHALCONTEXT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - callobj.h
api_name:
 - CALLFRAME_MARSHALCONTEXT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# __MIDL_ICallFrame_0004 structure


## -description


Provides information about the context in which marshalling should be carried out.


## -struct-fields




### -field fIn

<b>TRUE</b> if the in parameter values are to be marshaled and <b>FALSE</b> if the out parameter values are to be marshaled. The in parameter values are marshaled on the client side and the out parameter values are marshaled on the server side.


### -field dwDestContext

Context in which unmarshaling is to be carried out.


### -field pvDestContext

Context in which unmarshaling is to be carried out.


### -field punkReserved

 


### -field guidTransferSyntax

The transfer syntax for which the marshalling should occur.



#### - mshlmgr

This parameter should be <b>NULL</b>.


## -see-also




<a href="https://msdn.microsoft.com/dcb82ff2-56e4-4c7e-a621-7ffd0f1a9d8e">CLSCTX</a>



<a href="https://msdn.microsoft.com/56a75123-f402-4187-af13-d31f72a5f094">ICallFrame</a>



<a href="https://msdn.microsoft.com/66de8d71-c27c-41bd-a741-02de5c779290">ICallUnmarshal</a>
 

 

