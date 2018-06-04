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

# OleUICanConvertOrActivateAs function


## -description


Determines if there are any OLE object classes in the registry that can be used to convert or activate the specified CLSID from.




## -parameters




### -param rClsid [in]

The CLSID of the class for which the information is required.


### -param fIsLinkedObject [in]

<b>TRUE</b> if the original object is a linked object; <b>FALSE</b> otherwise.


### -param wFormat [in]

Format of the original class.


## -returns



This function returns <b>TRUE</b> if the specified class can be converted to another class; <b>FALSE</b> otherwise.




## -remarks



<b>OleUICanConvertOrActivateAs</b> searches the registry for classes that include wFormat in their \Conversion\Readable\Main, \Conversion\ReadWriteable\Main, and \DataFormats\DefaultFile entries.



This function is useful for determining if a <b>Convert...</b> menu item should be disabled. If the CF_DISABLEDISPLAYASICON flag is specified in the call to <a href="https://msdn.microsoft.com/3af4b321-cea2-4f88-ae22-2dcefbb2c2ad">OleUIConvert</a>, then the <b>Convert...</b> menu item should be enabled only if <b>OleUICanConvertOrActivateAs</b> returns <b>TRUE</b>.





## -see-also




<a href="https://msdn.microsoft.com/3af4b321-cea2-4f88-ae22-2dcefbb2c2ad">OleUIConvert</a>
 

 

