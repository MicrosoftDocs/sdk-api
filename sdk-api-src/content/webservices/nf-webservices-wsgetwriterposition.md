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

# WsGetWriterPosition function


## -description



        Returns the current position of the writer.  This can only be used on a 
        writer that is set to an XmlBuffer. When writing to a buffer, the position
        represents the xml node before which new data will be placed.
      


## -parameters




### -param writer [in]


          The writer for which the current position will be obtained.
        


### -param nodePosition [out]


          The current position of the writer is returned here.
        


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">

One or more arguments are invalid.

</td>
</tr>
</table>
 




## -remarks




        See <a href="https://msdn.microsoft.com/40ca058c-04e1-4358-b330-360a094a8791">WS_XML_NODE_POSITION</a> for more information on using positions.
      


        It may be useful to call <a href="https://msdn.microsoft.com/56bf55f8-978c-4f03-9ace-f992530927c2">WsWriteEndStartElement</a> to force an element to be committed before
        obtaining the position.
      



