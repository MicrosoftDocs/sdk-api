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

# IFsrmFileScreen::ApplyTemplate


## -description


<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/86ee74e0-64d5-478a-8150-0f4b37e56694">MSFT_FSRMFileScreen</a> class.]

Applies the property values of the specified file screen template to this file screen 
    object.


## -parameters




### -param fileScreenTemplateName [in]

The name of the file screen template. The string is limited to 4,000 characters.


## -returns



The method returns the following return values.




## -remarks



To save the changes, call the 
    <a href="https://msdn.microsoft.com/81c9b1db-7756-47b2-98e6-8e819d93cd0f">IFsrmFileScreen::Commit</a> method.

The specified template must be a committed template; you cannot apply a newly created template that has not 
    been committed.


#### Examples

For an example, see 
     <a href="https://msdn.microsoft.com/1b5227e7-4272-4e23-ba55-d6161e2987bc">Defining a File Screen</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/69b831a1-c935-4de0-b222-009bafc45ec5">IFsrmFileScreen</a>



<a href="https://msdn.microsoft.com/86ee74e0-64d5-478a-8150-0f4b37e56694">MSFT_FSRMFileScreen</a>
 

 

