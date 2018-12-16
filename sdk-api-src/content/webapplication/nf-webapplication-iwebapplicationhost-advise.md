---
UID: NF:webapplication.IWebApplicationHost.Advise
title: IWebApplicationHost::Advise
author: windows-sdk-content
description: Establishes a connection to allow a client to receive events.
old-location: debug\iwebapplicationhost_advise.htm
tech.root: debug_wwahost
ms.assetid: 94c016cb-f043-4ea6-a5d1-f3486b55c97f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Advise, Advise method [Debugging Windows Store apps], Advise method [Debugging Windows Store apps],IWebApplicationHost interface, IWebApplicationHost interface [Debugging Windows Store apps],Advise method, IWebApplicationHost.Advise, IWebApplicationHost::Advise, debug.iwebapplicationhost_advise, webapplication/IWebApplicationHost::Advise
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
 - IWebApplicationHost.Advise
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWebApplicationHost::Advise


## -description


Establishes a connection to allow a client to receive events.


## -parameters




### -param interfaceId [in]

Type: <b>REFIID</b>

The identifier of the event interface.


### -param callback [in]

Type: <b><a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>*</b>

The caller's event interface.


### -param cookie [out]

Type: <b>DWORD*</b>

A token that uniquely identifies this connection.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/ac0ace8e-3f83-44be-baee-560c5472aa08">IWebApplicationHost</a>



<a href="https://msdn.microsoft.com/daab1a3f-1f84-4559-bdc0-be8f1fb28904">IWebApplicationHost::Unadvise</a>
 

 

