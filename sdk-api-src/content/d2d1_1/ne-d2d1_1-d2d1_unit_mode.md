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

# D2D1_UNIT_MODE enumeration


## -description


Specifies how units in Direct2D will be interpreted.


## -enum-fields




### -field D2D1_UNIT_MODE_DIPS

Units will be interpreted as device-independent pixels (1/96").


### -field D2D1_UNIT_MODE_PIXELS

Units will be interpreted as pixels.


### -field D2D1_UNIT_MODE_FORCE_DWORD




## -remarks



Setting the unit mode to <b>D2D1_UNIT_MODE_PIXELS</b> is similar to setting the <a href="https://msdn.microsoft.com/a54dd628-c2a2-4b04-9ced-7749a395f187">ID2D1DeviceContext</a> dots per inch (dpi) to 96. However, Direct2D still checks the dpi to determine the threshold for enabling vertical antialiasing for text, and when the unit mode is restored, the dpi will be remembered.




## -see-also




<a href="https://msdn.microsoft.com/d1c6476d-151b-4f2a-9aae-726de219567c">ID2D1DeviceContext::GetUnitMode</a>



<a href="https://msdn.microsoft.com/a5774b9a-4458-47e7-821a-4ac4b70468e3">ID2D1DeviceContext::SetUnitMode</a>
 

 

