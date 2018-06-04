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

# CInstance::SetWBEMINT64(LPCWSTR,const LONGLONG)


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/aed29340-eb64-437d-b7e8-4f0e49c8288a">CInstance</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>SetWBEMINT64(LPCWSTR, const LONGLONG&amp;)</b> method sets a 64-bit integer value.


## -parameters




### -param name

Name of the 64-bit integer property that is set.


### -param i64Value [ref]

Value assigned to the 64-bit integer property.


## -returns



Returns <b>TRUE</b> if the operation is successful and <b>FALSE</b> if an attempt was made to set a nonexistent property or a property that is not a 64-bit integer.  More information is available in the log file, Framework.log.




## -remarks



The provider framework currently uses a CHString type to set the 64-bit integer  rather than a WBEMINT64 type.




## -see-also




<a href="https://msdn.microsoft.com/aed29340-eb64-437d-b7e8-4f0e49c8288a">CInstance</a>



<a href="https://msdn.microsoft.com/b51d0c51-3b72-4358-8fc3-d1dbc298b4d9">CInstance::GetWBEMINT64</a>
 

 

