---
UID: NF:objidl.IInitializeSpy.PreInitialize
title: IInitializeSpy::PreInitialize
author: windows-sdk-content
description: Performs initialization steps required before calling the CoInitializeEx function.
old-location: com\iinitializespy_preinitialize.htm
tech.root: com
ms.assetid: f5b345d1-ab37-401a-9cb4-b01ef7254fc8
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: IInitializeSpy interface [COM],PreInitialize method, IInitializeSpy.PreInitialize, IInitializeSpy::PreInitialize, PreInitialize, PreInitialize method [COM], PreInitialize method [COM],IInitializeSpy interface, _com_iinitializespy_preinitialize, com.iinitializespy_preinitialize, objidl/IInitializeSpy::PreInitialize
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ObjIdl.h
api_name:
 - IInitializeSpy.PreInitialize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IInitializeSpy::PreInitialize


## -description


Performs initialization steps required before calling the <a href="https://msdn.microsoft.com/ffb79c0f-aeda-4ea1-aea8-afb79109837f">CoInitializeEx</a> function.


## -parameters




### -param dwCoInit [in]

The apartment type passed to <a href="https://msdn.microsoft.com/ffb79c0f-aeda-4ea1-aea8-afb79109837f">CoInitializeEx</a>, specified as a member of the <a href="https://msdn.microsoft.com/0ac4a809-05f8-46d7-8e79-9d4e88b487f4">COINIT</a> enumeration.


### -param dwCurThreadAptRefs [in]

The number of times <a href="https://msdn.microsoft.com/ffb79c0f-aeda-4ea1-aea8-afb79109837f">CoInitializeEx</a> has been called on this thread.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/ffb79c0f-aeda-4ea1-aea8-afb79109837f">CoInitializeEx</a>



<a href="https://msdn.microsoft.com/9cf1a3fa-dbc6-4760-a9e9-ef237737acfb">IInitializeSpy</a>
 

 

