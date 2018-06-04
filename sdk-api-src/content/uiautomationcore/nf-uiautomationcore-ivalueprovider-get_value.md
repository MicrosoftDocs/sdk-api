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

# IValueProvider::get_Value


## -description


The value of the control.

This property is read-only.


## -parameters


## -remarks




Single-line edit controls support programmatic access to their contents by implementing <a href="https://msdn.microsoft.com/e6adbc23-dbfe-4dd2-82d9-66ce16de3338">IValueProvider</a> (in addition to <a href="https://msdn.microsoft.com/8bd53f1e-731f-420b-a529-ca3f6c3fd97c">ITextProvider</a>). However, multi-line edit controls do not implement <b>IValueProvider</b>.



To retrieve the textual contents of multi-line edit controls, the controls must implement <a href="https://msdn.microsoft.com/8bd53f1e-731f-420b-a529-ca3f6c3fd97c">ITextProvider</a>. However, <b>ITextProvider</b> does not support setting the value of a control.



<a href="https://msdn.microsoft.com/e6adbc23-dbfe-4dd2-82d9-66ce16de3338">IValueProvider</a> does not support the retrieval of formatting information or substring values. Implement <a href="https://msdn.microsoft.com/8bd53f1e-731f-420b-a529-ca3f6c3fd97c">ITextProvider</a> in these scenarios.

        




## -see-also




<a href="https://msdn.microsoft.com/e6adbc23-dbfe-4dd2-82d9-66ce16de3338">IValueProvider</a>



<a href="https://msdn.microsoft.com/8928c889-0e0a-439f-87e8-a9d121fcf73f">UI Automation Providers Overview</a>
 

 

