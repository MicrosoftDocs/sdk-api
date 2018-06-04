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

# IValueProvider::get_IsReadOnly


## -description


Indicates whether the value of a control is read-only. 

This property is read-only.


## -parameters


## -remarks




            A control should have its IsEnabled property (<a href="uiauto_automation_element_propids.htm">UIA_IsEnabledPropertyId</a>) set to <b>TRUE</b> and its <b>IValueProvider::IsReadOnly</b> 
            property set to <b>FALSE</b> before allowing a call to <a href="https://msdn.microsoft.com/af555ac6-5abd-4019-804b-68f9ed3be801">IValueProvider::SetValue</a>.
        




## -see-also




<a href="https://msdn.microsoft.com/e6adbc23-dbfe-4dd2-82d9-66ce16de3338">IValueProvider</a>



<a href="https://msdn.microsoft.com/8928c889-0e0a-439f-87e8-a9d121fcf73f">UI Automation Providers Overview</a>
 

 

