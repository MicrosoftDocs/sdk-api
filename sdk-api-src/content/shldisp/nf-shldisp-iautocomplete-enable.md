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

# IAutoComplete::Enable


## -description


Enables or disables autocompletion.


## -parameters




### -param fEnable [in]

Type: <b>BOOL</b>

A value that is set to <b>TRUE</b> to enable autocompletion, or <b>FALSE</b> to disable it.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, or a COM error value otherwise.




## -remarks



Autocompletion is enabled by default. Applications need only to call this method to disable autocompletion or to reenable it if it has been disabled.




## -see-also




<a href="https://msdn.microsoft.com/bed6eb41-3086-4af7-8c75-651da9dba3b2">IAutoComplete</a>
 

 

