---
UID: NF:webservices.WsGetWriterPosition
title: WsGetWriterPosition function
author: windows-sdk-content
description: Returns the current position of the writer. This can only be used on a writer that is set to an XmlBuffer. When writing to a buffer, the position represents the xml node before which new data will be placed.
old-location: wsw\wsgetwriterposition.htm
old-project: wsw
ms.assetid: 0c0fbd78-ed4f-40da-a63d-a2f38136ecb3
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: WsGetWriterPosition, WsGetWriterPosition function [Web Services for Windows], webservices/WsGetWriterPosition, wsw.wsgetwriterposition
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WS_SECURITY_ALGORITHM_PROPERTY_ID
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WebServices.dll
api_name:
 - WsGetWriterPosition
product: Windows
targetos: Windows
req.lib: WebServices.lib
req.dll: WebServices.dll
req.irql: 
req.product: Windows Address Book 5.0
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
      



