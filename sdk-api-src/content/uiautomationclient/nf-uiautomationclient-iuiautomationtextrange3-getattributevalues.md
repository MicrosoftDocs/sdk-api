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

# IUIAutomationTextRange3::GetAttributeValues


## -description


Returns all of the requested text attribute values for a text range in a single cross-process call.  This is equivalent to calling <a href="https://msdn.microsoft.com/7a77774e-7be0-473e-a0c9-e1aa108549e1">GetAttributeValue</a>, except it can retrieve multiple values instead of just one.


## -parameters




### -param attributeIds [in]

A list of <a href="https://msdn.microsoft.com/67d86817-6a3f-4047-88d9-34f33f52a563">text attribute identifiers</a>.


### -param attributeIdCount [in]

The number of <a href="https://msdn.microsoft.com/67d86817-6a3f-4047-88d9-34f33f52a563">text attribute identifiers</a> in the <i>attributeIds</i> list.


### -param attributeValues [out, retval]

A <b>SAFEARRAY</b> of <b>VARIANT</b> containing values to corresponding text attributes for a text range.


## -returns



Returns <b>S_OK</b> if successful, otherwise an <b>HRESULT</b> error code.




## -remarks



<b>GetAttributeValues</b> only gets the text attributes that are supplied in the call.




## -see-also




<a href="https://msdn.microsoft.com/3491996E-89EF-496D-94B6-FF8D121D3828">IUIAutomationTextRange3</a>



<a href="https://msdn.microsoft.com/98a82ff8-f4b9-4f62-ae69-31a2c18de70e">UI Automation Support for Textual Content</a>
 

 

