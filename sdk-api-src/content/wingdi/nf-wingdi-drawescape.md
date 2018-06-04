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

# DrawEscape function


## -description


The <b>DrawEscape</b> function provides drawing capabilities of the specified video display that are not directly available through the graphics device interface (GDI).


## -parameters




### -param hdc [in]

A handle to the DC for the specified video display.


### -param iEscape

TBD


### -param cjIn

TBD


### -param lpIn

TBD




#### - cbInput [in]

The number of bytes of data pointed to by the <i>lpszInData</i> parameter.


#### - lpszInData [in]

A pointer to the input structure required for the specified escape.


#### - nEscape [in]

The escape function to be performed.


## -returns



If the function is successful, the return value is greater than zero except for the QUERYESCSUPPORT draw escape, which checks for implementation only.

If the escape is not implemented, the return value is zero.

If an error occurred, the return value is less than zero.




## -remarks



When an application calls the <b>DrawEscape</b> function, the data identified by <i>cbInput</i> and <i>lpszInData</i> is passed directly to the specified display driver.




## -see-also




<a href="https://msdn.microsoft.com/9ff68d16-0f27-4cc8-932a-b2063cfed135">Device Context Functions</a>



<a href="https://msdn.microsoft.com/1fa97368-8931-4687-b37f-ed4db949a150">Device Contexts Overview</a>
 

 

