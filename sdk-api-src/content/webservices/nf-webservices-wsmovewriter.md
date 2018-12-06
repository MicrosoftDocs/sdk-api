---
UID: NF:webservices.WsMoveWriter
title: WsMoveWriter function
author: windows-sdk-content
description: Moves the current position of the writer as specified by the moveTo parameter.
old-location: wsw\wsmovewriter.htm
tech.root: wsw
ms.assetid: f8eace53-9fa5-466a-8894-3c8b8fe049e3
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WsMoveWriter, WsMoveWriter function [Web Services for Windows], webservices/WsMoveWriter, wsw.wsmovewriter
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: WebServices.lib
req.dll: WebServices.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WebServices.dll
api_name:
 - WsMoveWriter
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WsMoveWriter function


## -description


Moves the current position of the writer as specified by the moveTo parameter.
      


## -parameters




### -param writer [in]

The writer to move.
        


### -param moveTo [in]

The relative position to move the writer.
        


### -param found

If this is non-<b>NULL</b>, then whether or not the new position could be moved to is returned here.
        

If this is <b>NULL</b>, and the position could not be moved to, then the function will return <b>WS_E_INVALID_FORMAT</b>.
        (See <a href="https://msdn.microsoft.com/96285557-8317-4875-b634-e2eacd605901">Windows Web Services Return Values</a>.) 


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
</table>
 




## -remarks



This can only be used on a writer that is set to an <a href="https://msdn.microsoft.com/75f1df70-4dc9-4365-9005-5eaca6688f16">WS_XML_BUFFER</a>.
      

If the found parameter is not <b>NULL</b>, then it will indicate there whether or not it could
        move to the requested node and return NOERROR.
      

If the found parameter is <b>NULL</b>, and the requested node is not found, it will return <b>WS_E_INVALID_FORMAT</b>.
      

Once positioned, the writer will then insert new data before the position specified.
      



