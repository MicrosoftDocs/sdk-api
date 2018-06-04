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

# IDirectDrawVideo::GetFourCCCodes


## -description



The <code>GetFourCCCodes</code> method retrieves the multimedia format type.




## -parameters




### -param pCount

Pointer to the number of FOURCC codes in the <i>pCodes</i> array.


### -param pCodes

Pointer to an array of <b>DWORD</b> media tags formerly used for Microsoft multimedia types.


## -returns



Returns an <b>HRESULT</b> value.




## -remarks



In the original Windows multimedia APIs, media types were tagged with 32-bit values created from four 8-bit characters and were known as <i>FOURCC</i> codes. Because FOURCC codes are unique, a one-to-one mapping has been made possible by allocating a range of 4 billion GUIDs representing FOURCCs.

This method retrieves the FOURCC codes that the current display driver can support. The number available is obtained by calling the method with a valid <i>pCount</i> pointer, but with <i>pCodes</i> set to <b>NULL</b>. In this case, the <i>pCount</i> variable will be filled in with the number of FOURCC codes available. An application can then allocate enough <b>DWORD</b> values for this many FOURCC codes and call the method again with the array pointer in <i>pCodes</i>.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/b918bf3b-b91b-40fb-abb8-4115a4f254bb">IDirectDrawVideo Interface</a>
 

 

