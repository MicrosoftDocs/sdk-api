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

# IEnumStreamIdMap::Next


## -description



The <code>Next</code> method retrieves the next <i>n</i> elements in the collection.




## -parameters




### -param cRequest [in]

The number of elements to retrieve.


### -param pStreamIdMap [in, out]

Address of a user-allocated array containing <i>cRequest</i> elements that will receive the retrieved <a href="https://msdn.microsoft.com/75f41d9f-00a1-47e1-8b42-64de1e6abbdb">STREAM_ID_MAP</a> structures.


### -param pcReceived [out]

Receives the number of elements actually retrieved.


## -returns



Returns S_OK if successful. If the method fails,an <b>HRESULT</b> error code is returned.




## -remarks



If <i>cRequest</i> &gt;= 0 and <i>pcReceived</i> is not <b>NULL</b>, upon return <i>pcReceived</i> contains the number of stream ID maps remaining in the collection.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/8bca9255-2bc8-408b-9127-e3fe050fcf01">IEnumStreamIdMap Interface</a>
 

 

