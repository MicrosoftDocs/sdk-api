---
UID: NF:webservices.WsSetWriterPosition
title: WsSetWriterPosition function
author: windows-sdk-content
description: Sets the current position of the writer. The position must have been obtained by a call to WsGetReaderPosition or WsGetWriterPosition.
old-location: wsw\wssetwriterposition.htm
old-project: wsw
ms.assetid: 1d23bda1-d1da-44d4-9a9d-258bba200b29
ms.author: windowssdkdev
ms.date: 05/18/2018
ms.keywords: WsSetWriterPosition, WsSetWriterPosition function [Web Services for Windows], webservices/WsSetWriterPosition, wsw.wssetwriterposition
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps | UWP apps]
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
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	WebServices.dll
api_name:
-	WsSetWriterPosition
product: Windows
targetos: Windows
req.lib: WebServices.lib
req.dll: WebServices.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WsSetWriterPosition function


## -description



        Sets the current position of the writer.  The position must have been obtained by a 
        call to <a href="https://msdn.microsoft.com/91e543f3-7325-4a90-9b99-c98918478853">WsGetReaderPosition</a> or <a href="https://msdn.microsoft.com/0c0fbd78-ed4f-40da-a63d-a2f38136ecb3">WsGetWriterPosition</a>.
      


## -parameters




### -param writer [in]


          The writer for which the current position will be set.
        


### -param nodePosition [in]


          The position to set the writer to.
        


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
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_INVALID_OPERATION</b></dt>
</dl>
</td>
<td width="60%">

The operation is not allowed due to the current state of the object.

</td>
</tr>
</table>
 




## -remarks




        This can only be used on a writer that is set to an <a href="https://msdn.microsoft.com/75f1df70-4dc9-4365-9005-5eaca6688f16">WS_XML_BUFFER</a>.
      


        When writing to a buffer, the position represents the xml node before which new data will be placed.
      


        See <a href="https://msdn.microsoft.com/40ca058c-04e1-4358-b330-360a094a8791">WS_XML_NODE_POSITION</a> for more information on using positions.
      



