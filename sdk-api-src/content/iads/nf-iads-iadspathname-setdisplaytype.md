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

# IADsPathname::SetDisplayType


## -description


The <b>IADsPathname::SetDisplayType</b> method specifies how to display the path  of an object. It can query for the path to be displayed in a string with both naming attributes and values, that is, "CN=Jeff Smith" or with values only, that is, "Jeff Smith".


## -parameters




### -param lnDisplayType

The display type of a path  as defined in  <a href="https://msdn.microsoft.com/bc57aa4d-99f6-483f-b027-9b66b0c3bad1">ADS_DISPLAY_ENUM</a>.


## -returns



This method supports the standard return values, including the following:




## -see-also




<a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>



<a href="https://msdn.microsoft.com/bc57aa4d-99f6-483f-b027-9b66b0c3bad1">ADS_DISPLAY_ENUM</a>



<a href="https://msdn.microsoft.com/9aa26d6c-aa86-4a23-a986-b8cb9057772a">IADsPathname</a>
 

 

