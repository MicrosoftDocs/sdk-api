---
UID: NE:wtypesbase.tagMSHCTX
title: tagMSHCTX
author: windows-sdk-content
description: Specifies the destination context, which is the process in which the unmarshaling is to be done.
old-location: com\mshctx.htm
tech.root: com
ms.assetid: d7d09ab2-96e7-48da-9292-0e4ca6cebe64
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: MSHCTX, MSHCTX enumeration [COM], MSHCTX_CROSSCTX, MSHCTX_DIFFERENTMACHINE, MSHCTX_INPROC, MSHCTX_LOCAL, MSHCTX_NOSHAREDMEM, _com_MSHCTX, com.mshctx, tagMSHCTX, wtypesbase/MSHCTX, wtypesbase/MSHCTX_CROSSCTX, wtypesbase/MSHCTX_DIFFERENTMACHINE, wtypesbase/MSHCTX_INPROC, wtypesbase/MSHCTX_LOCAL, wtypesbase/MSHCTX_NOSHAREDMEM
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: wtypesbase.h
req.include-header: WTypes.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wtypesbase.h
api_name:
 - MSHCTX
product: Windows
targetos: Windows
req.typenames: MSHCTX
req.redist: 
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
 

 

