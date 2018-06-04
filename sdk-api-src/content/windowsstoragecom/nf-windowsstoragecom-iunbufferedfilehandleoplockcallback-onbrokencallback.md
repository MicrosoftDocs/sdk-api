---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IUnbufferedFileHandleOplockCallback::OnBrokenCallback


## -description


Runs when the opportunistic lock for a handle that you get by calling the <a href="https://msdn.microsoft.com/D001CD90-A621-403C-B9BD-BE79471AF18F">IUnbufferedFileHandleProvider::OpenUnbufferedFileHandle</a> method is broken.


## -parameters






## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Implement this method to specify what your app should do when the opportunistic lock for a handle that you get by calling the <a href="https://msdn.microsoft.com/D001CD90-A621-403C-B9BD-BE79471AF18F">IUnbufferedFileHandleProvider::OpenUnbufferedFileHandle</a> method is broken.




## -see-also




<a href="https://msdn.microsoft.com/7418EDE0-D9E1-4D8C-84B0-CAE9BDF053E3">IUnbufferedFileHandleOplockCallback</a>



<a href="https://msdn.microsoft.com/D001CD90-A621-403C-B9BD-BE79471AF18F">IUnbufferedFileHandleProvider::OpenUnbufferedFileHandle</a>
 

 

