---
UID: NF:objidl.IInitializeSpy.PreUninitialize
title: IInitializeSpy::PreUninitialize
author: windows-sdk-content
description: Performs cleanup steps required before calling the CoUninitialize function.
old-location: com\iinitializespy_preuninitialize.htm
old-project: com
ms.assetid: 22f9c663-0c6e-4413-a3a3-21cbb5ce62c9
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: IInitializeSpy interface [COM],PreUninitialize method, IInitializeSpy.PreUninitialize, IInitializeSpy::PreUninitialize, PreUninitialize, PreUninitialize method [COM], PreUninitialize method [COM],IInitializeSpy interface, _com_iinitializespy_preuninitialize, com.iinitializespy_preuninitialize, objidl/IInitializeSpy::PreUninitialize
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: THDTYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ObjIdl.h
api_name:
 - IInitializeSpy.PreUninitialize
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IInitializeSpy::PreUninitialize


## -description


Performs cleanup steps required before calling the <a href="https://msdn.microsoft.com/9411cbed-fa3b-46f7-b677-6ada53324edc">CoUninitialize</a> function.


## -parameters




### -param dwCurThreadAptRefs [in]

The number of times <a href="https://msdn.microsoft.com/ffb79c0f-aeda-4ea1-aea8-afb79109837f">CoInitializeEx</a> has been called on this thread.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/9411cbed-fa3b-46f7-b677-6ada53324edc">CoUninitialize</a>



<a href="https://msdn.microsoft.com/9cf1a3fa-dbc6-4760-a9e9-ef237737acfb">IInitializeSpy</a>
 

 

