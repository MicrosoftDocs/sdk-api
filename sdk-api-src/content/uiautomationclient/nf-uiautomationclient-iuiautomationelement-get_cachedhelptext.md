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

# IUIAutomationElement::get_CachedHelpText


## -description


Retrieves the cached help text for the element.

This property is read-only.


## -parameters


## -remarks



This information is typically obtained from ToolTips.

<div class="alert"><b>Caution</b>  Do not retrieve the <b>CachedHelpText</b> property from a control that is based on the SysListview32 class. Doing so could cause the system to become unstable and data to be lost. A client application can discover whether a control is based on SysListview32 by retrieving the <a href="https://msdn.microsoft.com/7b5e9c75-5190-4cdd-9774-0c883747018c">CachedClassName</a> or <a href="https://msdn.microsoft.com/df019800-7467-48ef-8c16-0cb8c8d05ed5">CurrentClassName</a> property from the control.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/f7613ad1-0b75-46fb-b9ac-b1ae9eea4193">Automation Element Property IDs</a>



<a href="https://msdn.microsoft.com/02ecfecc-5c3d-458b-827a-a598b8f98916">CurrentHelpText</a>



<a href="https://msdn.microsoft.com/9e1f87b1-a204-4ca9-acf2-a40277012207">IUIAutomationElement</a>



<b>Reference</b>
 

 

