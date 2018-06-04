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

# MsiSummaryInfoSetPropertyA function


## -description


The 
<b>MsiSummaryInfoSetProperty</b> function sets a single summary information property.


<div class="alert"><b>Note</b>  The meaning of the property value depends on whether the summary information stream is for an installation database (.msi file), transform (.mst file) or patch (.msp file). See <a href="https://msdn.microsoft.com/b44b24b7-7fc4-4c3c-9d10-7e2f3c43cf36">Summary Property Descriptions</a> and <a href="https://msdn.microsoft.com/a5dd014f-21af-41f9-be75-1b139946179d">Summary Information Stream Property Set</a> for more information about summary information properties.</div>
<div> </div>



## -parameters




### -param hSummaryInfo [in]

Handle to summary information.


### -param uiProperty [in]

Specifies the property ID of the summary property being set. This parameter can be a property ID  listed in the <a href="https://msdn.microsoft.com/a5dd014f-21af-41f9-be75-1b139946179d">Summary Information Stream Property Set</a>.  This function does not set values for PID_DICTIONARY OR PID_THUMBNAIL property.


### -param uiDataType [in]

Specifies the type of property to set. This parameter can be a type listed in the 
<a href="https://msdn.microsoft.com/a5dd014f-21af-41f9-be75-1b139946179d">Summary Information Stream Property Set</a>.


### -param iValue [in]

Specifies the integer value.


### -param pftValue [in]

Specifies the file-time value.


### -param szValue [in]

Specifies the text value.


## -returns




					The 
<b>MsiSummaryInfoSetProperty</b> function returns the following values:




## -see-also




<a href="database_functions.htm">Summary Information Property Functions</a>



<a href="https://msdn.microsoft.com/a5dd014f-21af-41f9-be75-1b139946179d">Summary Information Stream Property Set</a>



<a href="https://msdn.microsoft.com/8e8f0987-c92b-43f3-a61a-35099188c629">Summaryinfo.Property</a>
 

 

