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

# TF_HALTCOND structure


## -description



The <b>TF_HALTCOND</b> structure is used to contain conditions of a range shift.




## -struct-fields




### -field pHaltRange

Pointer to an <a href="https://msdn.microsoft.com/b8889f7d-3228-4ecc-8d24-c04234d3101e">ITfRange</a> object that halts the shift. If the range shift encounters this range during the shift, the shift halts. This member can be <b>NULL</b>.


### -field aHaltPos

Contains one of the <a href="https://msdn.microsoft.com/d670666f-2915-4a23-b825-b534a015e37f">TfAnchor</a> values that specifies which anchor of <b>pHaltRange</b> the anchor will get shifted to if <b>pHaltRange</b> is encountered during the range shift. This member is ignored if <b>pHaltRange</b> is <b>NULL</b>.


### -field dwFlags

Contains a set of flags that modify the behavior of the range shift. This can be zero or the following value.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>TF_HF_OBJECT</td>
<td>The range shift halts if an embedded object is encountered.</td>
</tr>
</table>
 


## -see-also




<a href="https://msdn.microsoft.com/b8889f7d-3228-4ecc-8d24-c04234d3101e">ITfRange
      </a>



<a href="https://msdn.microsoft.com/1debec6d-f98f-45a4-aaa8-99b61f3583ef">
        ITfRange::ShiftEnd
      </a>



<a href="https://msdn.microsoft.com/f9f983b1-a5fa-4857-b73c-b879c566d6f6">
        ITfRange::ShiftStart
      </a>



<a href="https://msdn.microsoft.com/d670666f-2915-4a23-b825-b534a015e37f">
        TfAnchor
      </a>
 

 

