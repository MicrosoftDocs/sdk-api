---
UID: NF:objidl.IInitializeSpy.PostUninitialize
title: IInitializeSpy::PostUninitialize
author: windows-sdk-content
description: Performs cleanup steps required after calling the CoUninitialize function.
old-location: com\iinitializespy_postuninitialize.htm
tech.root: com
ms.assetid: f91a1a4a-4d0b-491e-a7c6-01596b5b9712
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IInitializeSpy interface [COM],PostUninitialize method, IInitializeSpy.PostUninitialize, IInitializeSpy::PostUninitialize, PostUninitialize, PostUninitialize method [COM], PostUninitialize method [COM],IInitializeSpy interface, _com_iinitializespy_postuninitialize, com.iinitializespy_postuninitialize, objidl/IInitializeSpy::PostUninitialize
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
 - IInitializeSpy.PostUninitialize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IInitializeSpy::PostUninitialize


## -description


Performs cleanup steps required after calling the <a href="https://msdn.microsoft.com/9411cbed-fa3b-46f7-b677-6ada53324edc">CoUninitialize</a> function.


## -parameters




### -param dwNewThreadAptRefs [in]

The number of calls to <a href="https://msdn.microsoft.com/9411cbed-fa3b-46f7-b677-6ada53324edc">CoUninitialize</a> remaining on this thread.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/9411cbed-fa3b-46f7-b677-6ada53324edc">CoUninitialize</a>



<a href="https://msdn.microsoft.com/9cf1a3fa-dbc6-4760-a9e9-ef237737acfb">IInitializeSpy</a>
 

 

