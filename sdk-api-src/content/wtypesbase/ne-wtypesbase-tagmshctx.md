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

# tagMSHCTX enumeration


## -description


Specifies the destination context, which is the process in which the unmarshaling is to be done. 


## -enum-fields




### -field MSHCTX_LOCAL

The unmarshaling process is local and has shared memory access with the marshaling process.


### -field MSHCTX_NOSHAREDMEM

The unmarshaling process does not have shared memory access with the marshaling process.


### -field MSHCTX_DIFFERENTMACHINE

The unmarshaling process is on a different computer. The marshaling code cannot assume that a particular piece of application code is installed on that computer.


### -field MSHCTX_INPROC

The unmarshaling will be done in another apartment in the same process. 



### -field MSHCTX_CROSSCTX

Create a new context in the current apartment.


### -field MSHCTX_RESERVED1




## -see-also




<a href="https://msdn.microsoft.com/c04c736c-8efe-438b-9d21-8b6ad53d36e7">CoGetMarshalSizeMax</a>



<a href="https://msdn.microsoft.com/0cb74adc-e192-4ae5-9267-02c79e301681">CoGetStandardMarshal</a>



<a href="https://msdn.microsoft.com/04ca1217-eac1-43e2-b736-8d7522ce8592">CoMarshalInterface</a>



<a href="https://msdn.microsoft.com/e6f08949-f27d-4aba-adff-eaf9c356a928">IMarshal</a>



<a href="https://msdn.microsoft.com/1d7d7e1c-a491-4625-97ae-0d4dc5d2fc20">IRpcChannelBuffer</a>



<a href="https://msdn.microsoft.com/f034436f-e24e-4b99-9fb9-b0400d3ebb72">IStdMarshalInfo</a>
 

 

