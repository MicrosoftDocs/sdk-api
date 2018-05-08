---
UID: NF:objidl.IInitializeSpy.PostInitialize
title: IInitializeSpy::PostInitialize
author: windows-driver-content
description: Performs initialization steps required after calling the CoInitializeEx function.
old-location: com\iinitializespy_postinitialize.htm
old-project: com
ms.assetid: bdef4089-93e6-4845-8dcc-1150d7a0d033
ms.author: windowsdriverdev
ms.date: 4/25/2018
ms.keywords: IInitializeSpy interface [COM],PostInitialize method, IInitializeSpy.PostInitialize, IInitializeSpy::PostInitialize, PostInitialize, PostInitialize method [COM], PostInitialize method [COM],IInitializeSpy interface, _com_iinitializespy_postinitialize, com.iinitializespy_postinitialize, objidl/IInitializeSpy::PostInitialize
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: THDTYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	ObjIdl.h
api_name:
-	IInitializeSpy.PostInitialize
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IInitializeSpy::PostInitialize


## -description


Performs initialization steps required after calling the <a href="https://msdn.microsoft.com/ffb79c0f-aeda-4ea1-aea8-afb79109837f">CoInitializeEx</a> function.


## -parameters




### -param hrCoInit [in]

The value returned by <a href="https://msdn.microsoft.com/ffb79c0f-aeda-4ea1-aea8-afb79109837f">CoInitializeEx</a>.


### -param dwCoInit [in]

The apartment type passed to <a href="https://msdn.microsoft.com/ffb79c0f-aeda-4ea1-aea8-afb79109837f">CoInitializeEx</a>, specified as a member of the <a href="https://msdn.microsoft.com/0ac4a809-05f8-46d7-8e79-9d4e88b487f4">COINIT</a> enumeration.


### -param dwNewThreadAptRefs [in]

The number of times <a href="https://msdn.microsoft.com/ffb79c0f-aeda-4ea1-aea8-afb79109837f">CoInitializeEx</a> has been called on this thread.


## -returns



This method returns the value that it intends the <a href="https://msdn.microsoft.com/ffb79c0f-aeda-4ea1-aea8-afb79109837f">CoInitializeEx</a> call to return to its caller. For more information, see the Remarks section.




## -remarks



The return value from <b>PostInitialize</b> is intended to be the returned <b>HRESULT</b> from the call to <a href="https://msdn.microsoft.com/ffb79c0f-aeda-4ea1-aea8-afb79109837f">CoInitializeEx</a>. This is always the case for a single active registration on this thread.

For cases where there are multiple registrations active on this thread, the returned <b>HRESULT</b> is arrived at by chaining of the various <b>PostInitialize</b> methods as follows: The COM determined <b>HRESULT</b> will be passed as the <i>hrCoInit</i> parameter to the first <b>PostInitialize</b> method called. The <b>HRESULT</b> from that <b>PostInitialize</b> call will be passed as the <i>hrCoInit</i> parameter to the next <b>PostInitialize</b> call. This chaining continues leading to the <b>HRESULT</b> from the last <b>PostInitialize</b> call being returned as the <b>HRESULT</b> from the call to <a href="https://msdn.microsoft.com/ffb79c0f-aeda-4ea1-aea8-afb79109837f">CoInitializeEx</a>.





## -see-also




<a href="https://msdn.microsoft.com/ffb79c0f-aeda-4ea1-aea8-afb79109837f">CoInitializeEx</a>



<a href="https://msdn.microsoft.com/9cf1a3fa-dbc6-4760-a9e9-ef237737acfb">IInitializeSpy</a>
 

 

