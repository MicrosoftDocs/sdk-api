---
UID: NE:objidl.tagBIND_FLAGS
title: tagBIND_FLAGS
author: windows-sdk-content
description: Controls aspects of moniker binding operations.
old-location: com\bind_flags.htm
old-project: com
ms.assetid: e8884e82-5de2-4a1f-b79c-d431afe9e87e
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: BIND_FLAGS, BIND_FLAGS enumeration [COM], BIND_JUSTTESTEXISTENCE, BIND_MAYBOTHERUSER, _com_BIND_FLAGS, com.bind_flags, objidl/BIND_FLAGS, objidl/BIND_JUSTTESTEXISTENCE, objidl/BIND_MAYBOTHERUSER, tagBIND_FLAGS
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Objidlbase.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: BIND_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Objidl.h
api_name:
 - BIND_FLAGS
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll
req.irql: 
req.product: ADAM
---

# tagBIND_FLAGS enumeration


## -description


Controls aspects of moniker binding operations.


## -enum-fields




### -field BIND_MAYBOTHERUSER

If this flag is specified, the moniker implementation can interact with the end user. Otherwise, the moniker implementation should not interact with the user in any way, such as by asking for a password for a network volume that needs mounting. If prohibited from interacting with the user when it otherwise would, a moniker implementation can use a different algorithm that does not require user interaction, or it can fail with the error MK_E_MUSTBOTHERUSER.


### -field BIND_JUSTTESTEXISTENCE

If this flag is specified, the caller is not interested in having the operation carried out, but only in learning whether the operation could have been carried out had this flag not been specified. For example, this flag lets the caller indicate only an interest in finding out whether an object actually exists by using this flag in a <a href="https://msdn.microsoft.com/b5ce39ff-3387-4f72-9aea-5a26eed3810c">IMoniker::BindToObject</a> call. Moniker implementations can, however, ignore this possible optimization and carry out the operation in full. Callers must be able to deal with both cases. 



## -see-also




<a href="https://msdn.microsoft.com/764f09c9-ff20-4ae2-b94f-4b0a1e117e49">BIND_OPTS</a>



<a href="https://msdn.microsoft.com/fb2aa8c1-dddc-480e-b544-61a1074125ef">BIND_OPTS2</a>



<a href="https://msdn.microsoft.com/7e668313-229a-4d04-b8a2-d5072c87a5b5">BIND_OPTS3</a>
 

 

