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

# OleUIAddVerbMenuA function


## -description


Adds the <b>Verb</b> menu for the specified object to the specified menu.




## -parameters




### -param lpOleObj [in, optional]

Pointer to the <a href="https://msdn.microsoft.com/58b32c87-39b6-4d64-9174-cf798ed302c2">IOleObject</a> interface on the selected object. If this is <b>NULL</b>, then a default disabled menu item is created. 


### -param lpszShortType [in, optional]

Pointer to the short name defined in the registry (AuxName==2) for the object identified with <i>lpOleObj</i>. If the string is not known, then <b>NULL</b> may be passed. If <b>NULL</b> is passed, <a href="https://msdn.microsoft.com/8ffffa01-d118-4955-84d1-a4659ba9ddc9">IOleObject::GetUserType</a> is called to retrieve it. If the caller has easy access to the string, it is faster to pass it in.


### -param hMenu [in]

Handle to the menu in which to make modifications.


### -param uPos [in]

Position of the menu item.


### -param uIDVerbMin [in]

The identifier value at which to start the verbs.


### -param uIDVerbMax [in]

 The maximum identifier value to be used for object verbs. If <i>uIDVerbMax</i> is 0, then no maximum identifier value is used.


### -param bAddConvert [in]

 Indicates whether to add a <b>Convert</b> item to the bottom of the menu (preceded by a separator).


### -param idConvert [in]

The identifier value to use for the <b>Convert</b> menu item, if <i>bAddConvert</i> is <b>TRUE</b>.


### -param lphMenu [out]

An <b>HMENU</b> pointer to the cascading verb menu if it's created. If there is only one verb, this will be filled with <b>NULL</b>.


## -returns



This function returns <b>TRUE</b> if <i>lpOleObj</i> was valid and at least one verb was added to the menu. A <b>FALSE</b> return indicates that <i>lpOleObj</i> was <b>NULL</b> and a disabled default menu item was created.  




## -remarks



If the object has one verb, the verb is added directly to the given menu.




