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

# GEO_ENUMNAMEPROC callback function


## -description


An application-defined callback function that processes enumerated geographical location information provided by the <a href="https://msdn.microsoft.com/0CB7AE4E-F48A-49A6-A5E8-F151D38CE11E">EnumSystemGeoNames</a> function. The <b>GEO_ENUMNAMEPROC</b> type defines a pointer to this callback function. <i>Geo_EnumNameProc</i> is a placeholder for the application-defined function name.


## -parameters




### -param Arg1


### -param Arg2








#### - GeoName [in]

A two-letter International Organization for Standardization (ISO) 3166-1 code or numeric United Nations (UN) Series M, Number 49  (M.49) code for a geographical location that is available on the operating system.


#### - data

Application-specific information that was specified by the data parameter when the application called the <a href="https://msdn.microsoft.com/0CB7AE4E-F48A-49A6-A5E8-F151D38CE11E">EnumSystemGeoNames</a> function.


## -returns



Returns <b>TRUE</b> to continue enumeration or <b>FALSE</b> otherwise.




## -remarks



An <i>Geo_EnumNameProc</i> function can carry out any desired task, and can use the information passed to it in the <i>data</i> parameter for any desired purpose. The application registers this function by passing its address to the <a href="https://msdn.microsoft.com/0CB7AE4E-F48A-49A6-A5E8-F151D38CE11E">EnumSystemGeoNames</a> function.

For information about two-letter ISO 3166-1 codes, see <a href="https://go.microsoft.com/fwlink/p/?linkid=859039">Country Codes - ISO 3166</a>.  For information about numeric UN M.49 codes, see <a href="https://go.microsoft.com/fwlink/p/?linkid=859018">Standard country or area codes for statistical use (M49)</a>.




## -see-also




<a href="https://msdn.microsoft.com/0CB7AE4E-F48A-49A6-A5E8-F151D38CE11E">EnumSystemGeoNames</a>



<a href="https://msdn.microsoft.com/7a548074-0782-45e1-8051-80c3b9d81885">National Language Support</a>



<a href="https://msdn.microsoft.com/7c72c4de-83be-4b7e-9ed8-b0236c1df8a4">National Language Support Functions</a>
 

 

