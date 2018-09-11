---
UID: NF:dmodshow.IDMOWrapperFilter.Init
title: IDMOWrapperFilter::Init
author: windows-sdk-content
description: The Init method initializes the DMO Wrapper filter with the specified DMO.
old-location: dshow\idmowrapperfilter_init.htm
tech.root: DirectShow
ms.assetid: 45f305b5-82bc-44c1-9af7-93aab371ed33
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: IDMOWrapperFilter interface [DirectShow],Init method, IDMOWrapperFilter.Init, IDMOWrapperFilter::Init, IDMOWrapperFilterInit, Init, Init method [DirectShow], Init method [DirectShow],IDMOWrapperFilter interface, dmodshow/IDMOWrapperFilter::Init, dshow.idmowrapperfilter_init
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dmodshow.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dmoguids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dmoguids.lib
 - Dmoguids.dll
api_name:
 - IDMOWrapperFilter.Init
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDMOWrapperFilter::Init


## -description



The <code>Init</code> method initializes the DMO Wrapper filter with the specified DMO.




## -parameters




### -param clsidDMO

Class identifier (CLSID) of the DMO.


### -param catDMO

CLSID that specifies the category of the DMO.


## -returns



Returns S_OK if successful. Otherwise, returns an <b>HRESULT</b> value indicating the cause of the error.




## -remarks



In some cases, the DMO Wrapper filter performs optimizations based on the category.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/c85b828c-095d-4991-85a8-65b96529f305">IDMOWrapperFilter Interface</a>
 

 

