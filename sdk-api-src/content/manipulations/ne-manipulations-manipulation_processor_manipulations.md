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

# MANIPULATION_PROCESSOR_MANIPULATIONS enumeration


## -description


The <b>MANIPULATION_PROCESSOR_MANIPULATIONS</b> enumeration different kinds of manipulation which can be applied on a target object.


## -enum-fields




### -field MANIPULATION_NONE

Indicates that no manipulations are performed.


### -field MANIPULATION_TRANSLATE_X

Indicates manipulation by moving the target across the horizontal axis.


### -field MANIPULATION_TRANSLATE_Y

Indicates manipulation by moving the target across the vertical axis.


### -field MANIPULATION_SCALE

Indicates manipulation by making the target larger or smaller.


### -field MANIPULATION_ROTATE

Indicates manipulation by rotating the target.


### -field MANIPULATION_ALL

Indicates all manipulations are enabled.


## -remarks




        Use this enumeration with the <a href="https://msdn.microsoft.com/1909394f-83ec-4e13-81af-3e6c70210865">SupportedManipulations</a> property to get and 
		  set the kind of manipulation data you want to receive from the <a href="https://msdn.microsoft.com/963f87c1-e128-4bd5-9f28-d49418f768fb">IManipulationProcessor</a> interface. 
		  You can combine different kinds of manipulations by a bitwise OR.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
        CoInitialize(0);

        hr = spIManipProc.CoCreateInstance(CLSID_ManipulationProcessor, NULL, CLSCTX_ALL);

        MANIPULATION_PROCESSOR_MANIPULATIONS mpm;
        spIManipProc-&gt;get_SupportedManipulations(&amp;mpm);    
        </pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/a4424d27-c618-4fbe-99f6-70c74d3e2966">Enumerations</a>
 

 

