---
UID: NF:strmif.IGraphConfigCallback.Reconfigure
title: IGraphConfigCallback::Reconfigure
author: windows-sdk-content
description: The Reconfigure method is a callback method passed to IGraphConfig::Reconfigure.
old-location: dshow\igraphconfigcallback_reconfigure.htm
tech.root: DirectShow
ms.assetid: b4f44639-b3b0-412e-8b71-e1f994dee0e6
ms.author: windowssdkdev
ms.date: 09/28/2018
ms.keywords: IGraphConfigCallback interface [DirectShow],Reconfigure method, IGraphConfigCallback.Reconfigure, IGraphConfigCallback::Reconfigure, IGraphConfigCallbackReconfigure, Reconfigure, Reconfigure method [DirectShow], Reconfigure method [DirectShow],IGraphConfigCallback interface, dshow.igraphconfigcallback_reconfigure, strmif/IGraphConfigCallback::Reconfigure
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IGraphConfigCallback.Reconfigure
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IGraphConfigCallback::Reconfigure


## -description



The <code>Reconfigure</code> method is a callback method passed to <a href="https://msdn.microsoft.com/924087c0-e3ad-437b-96e5-de39bbce2ea7">IGraphConfig::Reconfigure</a>.




## -parameters




### -param pvContext

Value passed in the <b>IGraphConfig::Reconfigure</b> method's <i>pvContext</i> parameter.


### -param dwFlags

Value passed in the <b>IGraphConfig::Reconfigure</b> method's <i>dwFlags</i> parameter.


## -returns



Returns S_OK if successful. Otherwise, returns an <b>HRESULT</b> value indicating the cause of the error.




## -remarks



If your application or filter calls <b>IGraphConfig::Reconfigure</b>, you must implement this method and pass it as a callback. The <b>IGraphConfig::Reconfigure</b> method obtains a lock on the filter graph before calling your <code>Reconfigure</code> method. Your method then handles all the other details of dynamic graph building.

If this method succeeds, <b>IGraphConfig::Reconfigure</b> tries to put all the filters in the graph back into a running state. If the method fails, <b>IGraphConfig::Reconfigure</b> returns whatever error code this method returned.

This method allows for specialized graph rebuilding. For a more straightforward approach to dynamic graph building, see <a href="https://msdn.microsoft.com/e8cfac8e-df89-444d-bcc7-0cbc7ab5a592">IGraphConfig::Reconnect</a>.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/b7856181-1616-4984-bf5e-402140ab7b4e">IGraphConfigCallback Interface</a>
 

 

