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

# IFsrmClassificationManager2::ClassifyFiles


## -description


This method is used to perform bulk enumeration, setting, and clearing of file 
    properties.


## -parameters




### -param filePaths [in]

A list of the file paths.  The <b>SAFEARRAY</b> contains variants of type 
      <b>VT_BSTR</b>. For each item in the array, use the <b>bstrVal</b> member 
      to access the property name.


### -param propertyNames [in]

A list of the property names.  The <b>SAFEARRAY</b> contains variants of type 
      <b>VT_BSTR</b>. For each item in the array, use the <b>bstrVal</b> member 
      to access the property name.


### -param propertyValues [in]

A list of the property values.


### -param options [in]

Options for the operation as enumerated by the 
      <a href="https://msdn.microsoft.com/d909e244-344f-4da9-987c-de406c2dc359">FsrmGetFilePropertyOptions</a> enumeration. The 
      default value is <b>FsrmGetFilePropertyOptions_None</b>.


## -returns



The method returns the following return values.




## -see-also




<a href="https://msdn.microsoft.com/4a8e0426-792d-49d8-acf3-ab00480e24ac">FsrmClassificationManager</a>



<a href="https://msdn.microsoft.com/d909e244-344f-4da9-987c-de406c2dc359">FsrmGetFilePropertyOptions</a>



<a href="https://msdn.microsoft.com/6ff821e3-f0bd-4c66-8ced-edbbfbc8503b">IFsrmClassificationManager2</a>



<a href="https://msdn.microsoft.com/79571ae1-726e-491b-b41e-6cd10cdf3936">MSFT_FSRMClassification</a>
 

 

