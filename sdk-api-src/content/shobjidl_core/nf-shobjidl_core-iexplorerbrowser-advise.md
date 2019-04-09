---
UID: NF:shobjidl_core.IExplorerBrowser.Advise
title: IExplorerBrowser::Advise (shobjidl_core.h)
author: windows-sdk-content
description: Initiates a connection with IExplorerBrowser for event callbacks.
old-location: shell\IExplorerBrowser_Advise.htm
tech.root: shell
ms.assetid: b77f9c41-248e-4f16-a9ff-6ff5437df11c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Advise, Advise method [Windows Shell], Advise method [Windows Shell],IExplorerBrowser interface, IExplorerBrowser interface [Windows Shell],Advise method, IExplorerBrowser.Advise, IExplorerBrowser::Advise, _shell_IExplorerBrowser_Advise, shell.IExplorerBrowser_Advise, shobjidl_core/IExplorerBrowser::Advise
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
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
 - shobjidl_core.h
api_name:
 - IExplorerBrowser.Advise
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IExplorerBrowser::Advise


## -description


Initiates a connection with <a href="https://msdn.microsoft.com/da2cf5d4-5a68-4d18-807b-b9d4e2712c10">IExplorerBrowser</a> for event callbacks.


## -parameters




### -param psbe [in]

Type: <b><a href="https://msdn.microsoft.com/802d547f-41c2-4c4a-9f07-be615d7b86eb">IExplorerBrowserEvents</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/802d547f-41c2-4c4a-9f07-be615d7b86eb">IExplorerBrowserEvents</a> interface of the object to be advised of <a href="https://msdn.microsoft.com/da2cf5d4-5a68-4d18-807b-b9d4e2712c10">IExplorerBrowser</a> events.


### -param pdwCookie [out]

Type: <b>DWORD*</b>

When this method returns, contains a token that uniquely identifies the event listener.  This allows several event listeners to be subscribed at a time.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method is called by an implementer of  <a href="https://msdn.microsoft.com/802d547f-41c2-4c4a-9f07-be615d7b86eb">IExplorerBrowserEvents</a>. The implementer (listener) is advised of ExplorerBrowser view and navigation events by callback of the methods of <b>IExplorerBrowserEvents</b>.

Call <b>IExplorerBrowser::Advise</b> to initiate an advisory connection prior to the first <a href="https://msdn.microsoft.com/da2cf5d4-5a68-4d18-807b-b9d4e2712c10">IExplorerBrowser</a> navigation.  Callbacks to event listeners are made as the browser is browsing.

The first browse happens synchronously to a call on <a href="https://msdn.microsoft.com/cbfe2348-9fdc-4839-bf8b-b2a65caefa4c">IExplorerBrowser::BrowseToObject</a>, or a similar method. Future callbacks happen asynchronously, as the browser browses.

When the connection is no longer needed, call method <a href="https://msdn.microsoft.com/a9b6b971-5676-4ceb-ab48-2350a1715b82">IExplorerBrowser::Unadvise</a> to terminate the connection.




## -see-also




<a href="https://msdn.microsoft.com/da2cf5d4-5a68-4d18-807b-b9d4e2712c10">IExplorerBrowser</a>



<a href="https://msdn.microsoft.com/54c97a55-a8d1-4635-a1e0-2f92d52ddc10">OnNavigationComplete</a>



<a href="https://msdn.microsoft.com/d4de3b81-4482-47c8-bb47-593aba484952">OnNavigationFailed</a>



<a href="https://msdn.microsoft.com/801d59f5-6e92-4e3c-938a-e94b43b7c6f1">OnViewCreated</a>
 

 

