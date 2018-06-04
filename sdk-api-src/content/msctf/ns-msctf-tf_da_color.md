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

# TF_DA_COLOR structure


## -description



The <b>TF_DA_COLOR</b> structure contains color data used in the display attributes for a range of text.




## -struct-fields




### -field type

Specifies the color type as defined in the <a href="https://msdn.microsoft.com/f692e188-d2f4-453b-a576-c6c05fd5f02a">TF_DA_COLORTYPE</a> enumeration.


### -field nIndex

Specifies the color as a system color index as defined in <a href="https://msdn.microsoft.com/165c1781-161e-4ab2-98c9-eec4e9098d09">GetSysColor</a>. This member is used only if <b>type</b> is equal to TF_CT_SYSCOLOR.


### -field cr

Specifies the color as an RGB value. This member is used only if <b>type</b> is equal to TF_CT_COLORREF.


## -see-also




<a href="https://msdn.microsoft.com/165c1781-161e-4ab2-98c9-eec4e9098d09">GetSysColor</a>



<a href="https://msdn.microsoft.com/f692e188-d2f4-453b-a576-c6c05fd5f02a">TF_DA_COLORTYPE
      </a>
 

 

