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

# tag_CompileStatusInfo structure


## -description


Describes an error for the <a href="https://msdn.microsoft.com/5e01c7ac-7090-4cde-b836-01fa9d3f27f5">IMofCompiler</a> interface.


## -struct-fields




### -field lPhaseError

TBD



#### 0

no error



#### 1

parsing error



#### 2

argument error



#### 3

errors occurred while storing the data.


### -field hRes

The actual error code.


### -field ObjectNum

Object that is at fault.


### -field FirstLine

First line number of the object.


### -field LastLine

Last line number of the object.


### -field dwOutFlags

Reserved.


## -remarks



The   <i>ObjectNum</i>, <i>FirstLine</i>, and <i>LastLine</i> parameters only contain values for errors that relate to a particular class or instance in the file.




## -see-also




<a href="https://msdn.microsoft.com/7f3cc061-839e-49c2-a225-452719f155a9">CompileBuffer</a>



<a href="https://msdn.microsoft.com/caf13a5c-2aca-4acb-8210-909737bf1022">CompileFile</a>



<a href="https://msdn.microsoft.com/39c5d621-0cdf-44e2-9ec0-c68299e85cb7">CreateBMOF</a>



<a href="https://msdn.microsoft.com/5e01c7ac-7090-4cde-b836-01fa9d3f27f5">IMofCompiler</a>
 

 

