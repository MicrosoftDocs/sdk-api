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

# WsWriteArray function


## -description


This operation sends a series of elements to an XML Writer.
      


## -parameters




### -param writer [in]


          A pointer to the Writer where the elements are written.
        


### -param localName [in]

A pointer to the localName of the repeating element.


### -param ns [in]

A pointer to the namespace of the repeating element.


### -param valueType [in]

The value type for the elements


### -param array


          A void pointer to the values written to <i>writer</i>.  The size of the items is determined by  value type.
          <div class="alert"><b>Note</b>  See <a href="https://msdn.microsoft.com/6075ed1c-ceb5-421a-8a76-3a64b9e6dbe3">WS_VALUE_TYPE</a> for more information.
        </div>
<div> </div>



### -param arraySize [in]


          The total byte length of the array.
        


### -param itemOffset [in]

The item offset within the array to write.
        


### -param itemCount [in]

The total number of items to write from the array.
        


### -param error [in, optional]

A  pointer to a <a href="https://msdn.microsoft.com/d5763d93-8eff-4df8-9a8a-a58aefabcb21">WS_ERROR</a> object where additional information about the error should be stored if the function fails.
                


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks




        This function is semantically equivalent to using <a href="https://msdn.microsoft.com/da23f5e6-504c-4e93-9190-7d8c41efc0da">WsWriteStartElement</a>,
        <a href="https://msdn.microsoft.com/c7b9d014-89b5-4959-b49e-ee2cdeb41f7c">WsWriteValue</a> and <a href="https://msdn.microsoft.com/cfb23857-bc51-4467-9aeb-6ce8810ae1b0">WsWriteEndElement</a> in a loop, but is more efficient.
      



