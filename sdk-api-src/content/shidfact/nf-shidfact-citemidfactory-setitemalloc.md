---
UID: NF:shidfact.CItemIDFactory.SetItemAlloc
title: CItemIDFactory::SetItemAlloc method
author: windows-driver-content
description: Provides the CItemIDFactory an IMalloc interface used to allocate and free item IDs.
old-location: shell\citemidfactory_setitemalloc.htm
old-project: shell
ms.assetid: 3E2BAAD9-5C16-4ECF-BADB-16B355439BA5
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: CItemIDFactory, CItemIDFactory interface [Windows Shell], SetItemAlloc method, CItemIDFactory::SetItemAlloc, SetItemAlloc method [Windows Shell], SetItemAlloc method [Windows Shell], CItemIDFactory interface, SetItemAlloc,CItemIDFactory.SetItemAlloc, shell.citemidfactory_setitemalloc, shidfact/CItemIDFactory::SetItemAlloc
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shidfact.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: SHELL_UI_COMPONENT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	shidfact.h
api_name:
-	CItemIDFactory.SetItemAlloc
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5.0
---

# CItemIDFactory::SetItemAlloc method


## -description


Provides the <a href="https://msdn.microsoft.com/8C13F1AF-3328-40B8-B5F8-6CDF753A7FA7">CItemIDFactory</a> an <a href="https://msdn.microsoft.com/047f281e-2665-4d6d-9a0b-918cd3339447">IMalloc</a> interface used to allocate and free item IDs.


## -parameters




### -param pmalloc [in, out]

A pointer to an <a href="https://msdn.microsoft.com/047f281e-2665-4d6d-9a0b-918cd3339447">IMalloc</a> interface.


## -returns



If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/8C13F1AF-3328-40B8-B5F8-6CDF753A7FA7">CItemIDFactory</a>



<a href="https://msdn.microsoft.com/16db01f3-4167-43f0-9ef7-34eec906e199">IDelegateFolder</a>
 

 

