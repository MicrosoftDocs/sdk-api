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

# IWbemQuery::Parse


## -description


The 
<b>IWbemQuery::Parse</b> method parses a query string.


## -parameters




### -param pszLang [in]

Language of the query. Must be either "WQL" or "SQL" (case-sensitive). Any other value will result in the method failing and <b>WBEM_E_INVALID_PARAMETER</b> being returned.


### -param pszQuery [in]

Valid WQL or SQL WMI query.


### -param uFlags [in]

Reserved for future use. Must be 0 (zero).


## -returns



This method returns an <b>HRESULT</b> indicating the status of the method call.




## -see-also




<a href="https://msdn.microsoft.com/4a0c0c1d-3d84-491f-8379-d164821fa71b">IWbemQuery</a>
 

 

