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

# ITextFont::IsEqual


## -description


Determines whether this text font object has the same properties as the specified text font object.


## -parameters




### -param pFont

Type: <b><a href="https://msdn.microsoft.com/e8e3ba98-808b-49c5-8764-96484fa33a6e">ITextFont</a>*</b>

The text font object to compare against.


### -param pValue






#### - pB

Type: <b>long*</b>

A variable that is <b>tomTrue</b> if the font objects have the same properties or <b>tomFalse</b> if they do not. This parameter can be <b>NULL</b>. 


## -returns



Type: <b>HRESULT</b>

If the text font objects have the same properties, the method succeeds and returns <b>S_OK</b>. If the text font objects do not have the same properties, the method fails and returns <b>S_FALSE</b>. For more information about COM error codes, see <a href="https://msdn.microsoft.com/15f3ae3e-1794-4948-a7aa-6309a703364b">Error Handling in COM</a>.




## -remarks



The text font objects are equal only if <i>pFont</i> belongs to the same Text Object Model (TOM) object as the current font object. The <b>ITextFont::IsEqual</b> method ignores entries for which either font object has an <a href="tomconstants.htm">tomUndefined</a>.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/e8e3ba98-808b-49c5-8764-96484fa33a6e">ITextFont</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/a15f0334-1a31-4bc3-bc1e-e5cf53112007">Text Object Model</a>
 

 

