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

# CVssWriterEx class


## -description


The <b>CVssWriterEx</b> class is an abstract base class that defines 
    the interface by which a writer synchronizes its state with VSS and other writers. 

The <b>CVssWriterEx</b> class inherits the methods of the <a href="https://msdn.microsoft.com/5d54c966-86ad-41af-82be-8a182b3d203a">CVssWriter</a> class.

Every writer must create an instance of the  
    <a href="https://msdn.microsoft.com/5d54c966-86ad-41af-82be-8a182b3d203a">CVssWriter</a> or <b>CVssWriterEx</b> class.

Objects that are derived from <b>CVssWriterEx</b> must supply implementations 
    for all of the pure virtual methods of both the <b>CVssWriterEx</b> and <a href="https://msdn.microsoft.com/5d54c966-86ad-41af-82be-8a182b3d203a">CVssWriter</a> classes.

A writer can override any or all of  the virtual 
    methods of <b>CVssWriterEx</b> and <a href="https://msdn.microsoft.com/5d54c966-86ad-41af-82be-8a182b3d203a">CVssWriter</a>. However, a writer can override the <a href="https://msdn.microsoft.com/542d479a-695a-4b1f-94e7-f2ffa08440b7">OnIdentify</a> or <a href="https://msdn.microsoft.com/4cb3b8f6-f702-4fba-a3cc-af84897cfd82">OnIdentifyEx</a> method, but not both.

<b xmlns:loc="http://microsoft.com/wdcml/l10n">CVssWriterEx</b> has these types of members:


## -see-also




<a href="https://msdn.microsoft.com/5d54c966-86ad-41af-82be-8a182b3d203a">CVssWriter</a>
 

 

