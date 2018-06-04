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

# IWSCProductList::get_Item


## -description


Returns one of the  types of providers on the computer.


## -parameters




### -param index [in]

The list of the providers.


### -param pVal [out]

A pointer to the <a href="https://msdn.microsoft.com/C637E67A-CED7-4235-AAF3-22730E9C7E91">IWscProduct</a> product information.


## -returns



If the method  succeeds, returns S_OK.

If the method  fails, returns a Win32 error code.




## -remarks



A provider is obtained by calling the <b>Item</b> method, which returns an interface pointer to an initialized <a href="https://msdn.microsoft.com/C637E67A-CED7-4235-AAF3-22730E9C7E91">IWscProduct</a> object.  The user is then able to retrieve the name, product state, and signature status through the methods of the <b>IWscProduct</b> interface.   




## -see-also




<a href="https://msdn.microsoft.com/81BC78F1-6F95-49D3-8EDD-EB7E13119A86">IWSCProductList</a>
 

 

