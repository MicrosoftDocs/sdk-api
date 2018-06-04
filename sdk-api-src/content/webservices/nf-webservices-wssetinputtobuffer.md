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

# WsSetInputToBuffer function


## -description


Sets Reader input to a specified XML buffer.
      Reader properties
        specified to <b>WsSetInputToBuffer</b>  override properties set by <a href="https://msdn.microsoft.com/0d4449aa-ffcc-41d9-99b1-7352edaf3700">WsCreateReader</a>.


        The reader does not modify <a href="https://msdn.microsoft.com/75f1df70-4dc9-4365-9005-5eaca6688f16">WS_XML_BUFFER</a> input data.
      <div class="alert"><b>Note</b>  
        It is permissible for more than one reader to read from the same <b>WS_XML_BUFFER</b>.</div>
<div> </div>



## -parameters




### -param reader [in]

A pointer to the <a href="https://msdn.microsoft.com/7acbe407-e91b-435a-82bc-acbbc13cfcfd">WS_XML_READER</a> object for which the input will be set.
        


### -param buffer [in]

A pointer to the XML buffer to read.
        


### -param properties

A pointer that references an array of optional Reader properties.  <div class="alert"><b>Note</b>  For more information see <a href="https://msdn.microsoft.com/8864d679-c321-45bb-b774-f05696d6098e">WS_XML_READER_PROPERTY</a>.</div>
<div> </div>.
        


### -param propertyCount [in]

The number of properties.


### -param error [in, optional]

A  pointer to a <a href="https://msdn.microsoft.com/d5763d93-8eff-4df8-9a8a-a58aefabcb21">WS_ERROR</a> object where additional information about the error should be stored if the function fails.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks




        When an XML Reader has an XML Buffer as an input source, the Reader can be used in a random access fashion, and
        the functions <a href="https://msdn.microsoft.com/91e543f3-7325-4a90-9b99-c98918478853">WsGetReaderPosition</a>, <a href="https://msdn.microsoft.com/cc879cc0-c8ca-457e-9ff1-ae220e31cb04">WsSetReaderPosition</a>, and <a href="https://msdn.microsoft.com/63d18407-f82b-4884-a162-2c8163e883e1">WsMoveReader</a> are available for use.
      



