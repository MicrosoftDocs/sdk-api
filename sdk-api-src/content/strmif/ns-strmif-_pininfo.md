---
UID: NS:strmif._PinInfo
title: "_PinInfo"
author: windows-sdk-content
description: The PIN_INFO structure contains information about a pin.
old-location: dshow\pin_info.htm
tech.root: DirectShow
ms.assetid: 67a837f3-8b81-4651-a0fa-fed7b61e71c2
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: PIN_INFO, PIN_INFO structure [DirectShow], PIN_INFOStructure, _PinInfo, dshow.pin_info, strmif/PIN_INFO
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - strmif.h
api_name:
 - PIN_INFO
product: Windows
targetos: Windows
req.typenames: PIN_INFO
req.redist: 
---

# _PinInfo structure


## -description



The <code>PIN_INFO</code> structure contains information about a pin.




## -struct-fields




### -field pFilter

Pointer to the <a href="https://msdn.microsoft.com/d8c09dc7-dae8-4b51-8da8-69e64928a091">IBaseFilter</a> interface of the owning filter.


### -field dir

Direction of the pin (input or output).


### -field achName

Name of the pin.


## -remarks



If the name of an output pin begins with a tilde (~), the filter graph manager ignores the pin when it builds a graph. During a call to <a href="https://msdn.microsoft.com/8ddcbb73-8220-4d70-9ab3-58d99fa8a958">IGraphBuilder::Connect</a>, <a href="https://msdn.microsoft.com/de3adac7-ff99-4415-9afc-e25ad420df59">IGraphBuilder::Render</a>, or <a href="https://msdn.microsoft.com/449aec08-c03e-41d6-8c04-0e871e532d11">IGraphBuilder::RenderFile</a>, if the pin appears on an intermediate filter, the filter graph manager does not render the pin. However, it renders the pin if you explicitly pass the pin to the <b>Connect</b> or <b>Render</b> method.

Use a tilde if the pin delivers a secondary stream that should not be rendered by default, or if the pin requires special code to render correctly. For example, DVD filters should use it for pins that deliver subpicture or closed captioning data. Video capture filters should use it for capture pins (but not preview pins).

The <b>pFilter</b> member has an outstanding reference count. The application must release the interface.




## -see-also




<a href="https://msdn.microsoft.com/378f6f43-5c05-4ae4-be24-956f9fc0cacf">DirectShow Structures</a>



<a href="https://msdn.microsoft.com/1a7c85ce-46f1-4928-9e2a-3a4bd96dc771">IPin::QueryPinInfo</a>
 

 

