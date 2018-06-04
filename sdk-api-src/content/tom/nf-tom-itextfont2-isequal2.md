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

# ITextFont2::IsEqual2


## -description


Determines whether this text font object has the same properties as the specified text font object.


## -parameters




### -param pFont [in]

Type: <b><a href="https://msdn.microsoft.com/d2d43bfd-7cdf-458a-822d-e3965bfe2284">ITextFont2</a>*</b>

The text font object to compare against.


### -param pB [out]

Type: <b>long*</b>

A <a href="About_Rich_Edit_Controls.htm">tomBool</a> value that is <b>tomTrue</b> if the font objects have the same properties, or <b>tomFalse</b> if they don't. This parameter can be <b>NULL</b>. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



 For two text font objects to be equal, both must belong to the same Text Object Model (TOM) object. 

The <b>ITextFont::IsEqual2</b> method ignores entries for which either font object has a <a href="tomconstants.htm">tomUndefined</a> value.




## -see-also




<a href="https://msdn.microsoft.com/d2d43bfd-7cdf-458a-822d-e3965bfe2284">ITextFont2</a>



<a href="https://msdn.microsoft.com/9c567d78-a915-4b44-bf52-61e72101c08b">ITextFont::IsEqual</a>
 

 

