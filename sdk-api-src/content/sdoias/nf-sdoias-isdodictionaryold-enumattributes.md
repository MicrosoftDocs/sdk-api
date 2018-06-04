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

# ISdoDictionaryOld::EnumAttributes


## -description


The 
<b>EnumAttributes</b> method retrieves the values of the specified attributes.


## -parameters




### -param Id [in, out]

On input, a pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/mt138335">VARIANT</a> 
       that specifies the attributes to enumerate. If the type of this 
       <b>VARIANT</b>, given by 
       <b>V_VT</b>(Id), is 
       <b>VT_EMPTY</b>, 
       <b>ISdoDictionaryOld::EnumAttributes</b> 
       enumerates all the attributes. If the type is <b>VT_I4</b>, then the value of the 
       <b>VARIANT</b> is the ID of the attribute 
       to enumerate.

On output, pointer to a 
       <a href="9ec8025b-4763-4526-ab45-390c5d8b3b1e">SAFEARRAY</a> that contains the IDs of 
       the enumerated attributes.


### -param pValues [out]

Pointer to a 
      <a href="9ec8025b-4763-4526-ab45-390c5d8b3b1e">SAFEARRAY</a> that contains 
      the values of the enumerated attributes.


## -returns



If the method succeeds the return value is <b>S_OK</b>.

If the method fails, the return value is one of the following error codes.




## -remarks



The parameters must not be <b>NULL</b>.

If VT(Id) = VT_EMPTY then all the attributes are returned. Otherwise VT(Id) should be <b>VT_I4</b> and only the attributes designed are retrieved.

When the method returns, Id is a <a href="9ec8025b-4763-4526-ab45-390c5d8b3b1e">SAFEARRAY</a> of the Ids returned, and <i>pValues</i> is a <b>SAFEARRAY</b> of the values returned.




## -see-also




<a href="https://msdn.microsoft.com/5aaa4008-3b39-4d1d-90db-79631e5bb6b9">ISdoDictionaryOld</a>
 

 

