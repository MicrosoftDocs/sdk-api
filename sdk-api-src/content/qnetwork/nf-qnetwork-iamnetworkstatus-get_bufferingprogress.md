---
UID: NF:qnetwork.IAMNetworkStatus.get_BufferingProgress
title: IAMNetworkStatus::get_BufferingProgress
author: windows-sdk-content
description: The get_BufferingProgress method retrieves a value indicating the buffering progress.
old-location: dshow\iamnetworkstatus_get_bufferingprogress.htm
old-project: DirectShow
ms.assetid: 76276bdc-1f19-4fb9-8ae9-1edeb5639741
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: IAMNetworkStatus interface [DirectShow],get_BufferingProgress method, IAMNetworkStatus.get_BufferingProgress, IAMNetworkStatus::get_BufferingProgress, IAMNetworkStatusget_BufferingProgress, dshow.iamnetworkstatus_get_bufferingprogress, get_BufferingProgress, get_BufferingProgress method [DirectShow], get_BufferingProgress method [DirectShow],IAMNetworkStatus interface, qnetwork/IAMNetworkStatus::get_BufferingProgress
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: qnetwork.h
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
req.typenames: AMExtendedSeekingCapabilities
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Qnetwork.h
api_name:
-	IAMNetworkStatus.get_BufferingProgress
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IAMNetworkStatus::get_BufferingProgress


## -description



The <code>get_BufferingProgress</code> method retrieves a value indicating the buffering progress.




## -parameters




### -param pBufferingProgress

Pointer to a variable that receives a value from 0 to 100, indicating what percentage has completed.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/51d56b76-f9fc-44e1-88f0-d35d861a4697">IAMNetworkStatus Interface</a>
 

 

