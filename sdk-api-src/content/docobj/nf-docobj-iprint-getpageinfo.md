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

# IPrint::GetPageInfo


## -description


Retrieves the number of a document's first page and the total number of pages.


## -parameters




### -param pnFirstPage [out]

A pointer to a variable that receives the page number of the first page. This parameter can be <b>NULL</b>, indicating that the caller is not interested in this number. If <a href="https://msdn.microsoft.com/352a4dc0-c79e-46e3-8212-55fd7d2916bc">IPrint::SetInitialPageNum</a> has been called, this parameter should contain the same value passed to that method. Otherwise, the value is the document's internal first page number.


### -param pcPages [out]

A pointer to a variable that receives the total number of pages in this document. This parameter can be <b>NULL</b>, indicating that the caller is not interested in this number.


## -returns



This method can return the standard return values E_UNEXPECTED and S_OK.




## -see-also




<a href="https://msdn.microsoft.com/eb0d15c0-8a34-4211-b840-29d5862cf767">IPrint</a>
 

 

