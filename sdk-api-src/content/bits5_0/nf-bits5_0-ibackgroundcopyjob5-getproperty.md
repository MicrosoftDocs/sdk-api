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

# IBackgroundCopyJob5::GetProperty


## -description


A generic method for getting BITS job properties.


## -parameters




### -param PropertyId [in]

The ID of the property that is being obtained specified as a <a href="https://msdn.microsoft.com/4ED7419E-3435-4F12-B293-1FDC24F40D63">BITS_JOB_PROPERTY_ID</a> enum value.


### -param PropertyValue






#### - pPropertyValue [out]

The property value returned as a BITS_JOB_PROPERTY_VALUE union.


## -returns



The method returns the following return values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/97481F9D-1F7B-473A-B288-A52E527478A0">IBackgroundCopyJob5</a>



<a href="https://msdn.microsoft.com/D5DB8A96-7417-4142-BA27-783314835CED">IBackgroundCopyJob5::SetProperty</a>
 

 

