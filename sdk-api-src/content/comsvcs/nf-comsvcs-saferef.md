---
UID: NF:comsvcs.SafeRef
title: SafeRef function
author: windows-sdk-content
description: SafeRef function
old-location: cos\saferef.htm
old-project: cossdk
ms.assetid: 14d75a5e-33e8-4b35-9813-3632454b89b6
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: SafeRef, SafeRef function [COM+], _cos_SafeRef, comsvcs/SafeRef, cos.saferef
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: TRACKING_COLL_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ComSvcs.dll
api_name:
 - SafeRef
product: Windows
targetos: Windows
req.lib: ComSvcs.lib
req.dll: ComSvcs.dll
req.irql: 
---

# SafeRef function


## -description


<p class="CCE_Message">[Do not use SafeRef in COM+. This function was used by objects in MTS to obtain a reference to itself. With COM+, this is no longer necessary.]


## -parameters




### -param rid [in]

A reference to the IID of the interface that the current object wants to pass to another object or client.


### -param pUnk [in]

A reference to the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface on the current object.


## -returns



If the function succeds, the return value is a pointer to the specified interface that can be passed outside the current object's context. Otherwise, the return value is <b>NULL</b>.




## -see-also




<a href="https://msdn.microsoft.com/50ccf75e-2652-4254-a771-af83cc9248b3">COM+ Contexts and Threading Models</a>



<a href="https://msdn.microsoft.com/1ecc5a8e-58d8-42e7-a543-da86ad966983">IMTxAS::SafeRef</a>
 

 

