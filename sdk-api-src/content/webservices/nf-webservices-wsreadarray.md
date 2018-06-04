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

# WsReadArray function


## -description



        Reads a series of elements from the reader and interprets their 
        content according to the specified value type.
      


## -parameters




### -param reader [in]


          The reader from which the array should be read.
        


### -param localName [in]

The localName of the repeating element.


### -param ns [in]

The namespace of the repeating element.


### -param valueType [in]

The value type to use to parse the content of each element.


### -param array


          The array to populate with parsed values.  The size of the array items is determined by the value type.
          See <a href="https://msdn.microsoft.com/6075ed1c-ceb5-421a-8a76-3a64b9e6dbe3">WS_VALUE_TYPE</a> for more information.
        


### -param arraySize [in]


          The size in bytes (not items) of the array.
        


### -param itemOffset [in]


          The item (not byte) offset within the array at which to read.
        


### -param itemCount [in]


          The number of items (not bytes) to read into the array.
        


### -param actualItemCount [out]


          The actual number of items that were read.  This may be less than itemCount even when there
          are more items remaining.  There are no more elements when this returns zero.
        


### -param error [in, optional]


          Specifies where additional error information should be stored if the function fails.
        


## -returns



This function can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_INVALID_FORMAT</b></dt>
</dl>
</td>
<td width="60%">

The input data was not in the expected format or did not have the expected value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_QUOTA_EXCEEDED</b></dt>
</dl>
</td>
<td width="60%">

A quota was exceeded.

</td>
</tr>
</table>
 




## -remarks




        This function is semantically equivalent to using <a href="https://msdn.microsoft.com/88661ae5-2112-4a41-8fcd-03c74f6ec170">WsReadStartElement</a>,
        <a href="https://msdn.microsoft.com/d2dbeaf1-29cb-4848-8188-7922fdc15091">WsReadValue</a> and <a href="https://msdn.microsoft.com/cd2e0e5a-9c73-4180-9c54-6742d87cb141">WsReadEndElement</a> in a loop, but is more efficient.
      


        This function can fail for any of the reasons listed in <a href="https://msdn.microsoft.com/60dacf3e-ebde-4247-be58-835565874ab6">WsReadNode</a>.
      



