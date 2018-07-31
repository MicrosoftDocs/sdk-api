---
UID: NF:strmif.IAMFilterGraphCallback.UnableToRender
title: IAMFilterGraphCallback::UnableToRender
author: windows-sdk-content
description: The UnableToRender method is called by the Filter Graph Manager if it cannot find any combination of filters to render the specified pin.
old-location: dshow\iamfiltergraphcallback_unabletorender.htm
old-project: DirectShow
ms.assetid: c7fa0eae-f950-423a-8a89-9a7619b27ce6
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IAMFilterGraphCallback interface [DirectShow],UnableToRender method, IAMFilterGraphCallback.UnableToRender, IAMFilterGraphCallback::UnableToRender, IAMFilterGraphCallbackUnableToRender, UnableToRender, UnableToRender method [DirectShow], UnableToRender method [DirectShow],IAMFilterGraphCallback interface, dshow.iamfiltergraphcallback_unabletorender, strmif/IAMFilterGraphCallback::UnableToRender
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
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
tech.root: 
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMFilterGraphCallback.UnableToRender
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IAMFilterGraphCallback::UnableToRender


## -description



The <code>UnableToRender</code> method is called by the Filter Graph Manager if it cannot find any combination of filters to render the specified pin.




## -parameters




### -param pPin

Specifies the <a href="https://msdn.microsoft.com/ad0ead4e-9f8e-4935-b220-306d665e50f4">IPin</a> interface of the pin that could not be rendered.


## -returns



If the return value is S_OK, this Filter Graph Manager attempts to render the pin again. For any other return value, including S_FALSE and other success codes, the Filter Graph Manager continues to build the graph as normal. Typically it will reject the current filter and attempt to use a different filter.




## -remarks



The Filter Graph Manager holds a graph-wide critical section while it calls this method. Therefore, the callback method should avoid calling any methods on the Filter Graph Manager, or any methods on filters that might change the graph state (such as disconnecting pins). Doing so might cause a deadlock or other unexpected behaviors. However, it is safe to query the pin for an interface or check the pin's preferred media type. The main use for this method would be to register a new filter, such as a decoder.

This method uses the thiscall calling convention, rather than __stdcall.




## -see-also




<a href="https://msdn.microsoft.com/064acc6a-ba2f-4394-a3bf-a9b70e30e07e">IAMFilterGraphCallback Interface</a>



<a href="https://msdn.microsoft.com/938ba1b0-822e-4871-8786-b7eeee243867">Intelligent Connect</a>
 

 

