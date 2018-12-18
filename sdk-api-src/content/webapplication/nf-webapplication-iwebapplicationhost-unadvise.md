---
UID: NF:webapplication.IWebApplicationHost.Unadvise
title: IWebApplicationHost::Unadvise
author: windows-sdk-content
description: Removes a previously established connection.
old-location: debug\iwebapplicationhost_unadvise.htm
tech.root: debug_wwahost
ms.assetid: daab1a3f-1f84-4559-bdc0-be8f1fb28904
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWebApplicationHost interface [Debugging Windows Store apps],Unadvise method, IWebApplicationHost.Unadvise, IWebApplicationHost::Unadvise, Unadvise, Unadvise method [Debugging Windows Store apps], Unadvise method [Debugging Windows Store apps],IWebApplicationHost interface, debug.iwebapplicationhost_unadvise, webapplication/IWebApplicationHost::Unadvise
ms.topic: method
req.header: webapplication.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Webapplication.idl
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
 - webapplication.h
api_name:
 - IWebApplicationHost.Unadvise
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWebApplicationHost::Unadvise


## -description


Removes a previously established connection.


## -parameters




### -param cookie [in]

Type: <b>DWORD</b>

A connection token previously returned from the <a href="https://msdn.microsoft.com/94c016cb-f043-4ea6-a5d1-f3486b55c97f">Advise</a> method.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/ac0ace8e-3f83-44be-baee-560c5472aa08">IWebApplicationHost</a>



<a href="https://msdn.microsoft.com/94c016cb-f043-4ea6-a5d1-f3486b55c97f">IWebApplicationHost::Advise</a>
 

 

