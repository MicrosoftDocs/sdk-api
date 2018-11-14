---
UID: NF:webservices.WsMoveReader
title: WsMoveReader function
author: windows-sdk-content
description: Moves the current position of the reader as specified by the moveTo parameter. This function can only be used on a reader that is set to an XmlBuffer.
old-location: wsw\wsmovereader.htm
tech.root: wsw
ms.assetid: 63d18407-f82b-4884-a162-2c8163e883e1
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: WsMoveReader, WsMoveReader function [Web Services for Windows], webservices/WsMoveReader, wsw.wsmovereader
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
 - WsMoveReader
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- WsMoveReader
: 
---

# WsMoveReader function


## -description


Moves the current position of the reader as specified by the <i>moveTo</i> parameter.
      
        This function can only be used on a reader that is set to an XmlBuffer.
      


## -parameters




### -param reader [in]

A pointer to the <b>XML Reader</b> object with the position to move.  The pointer must reference a valid <a href="https://msdn.microsoft.com/7acbe407-e91b-435a-82bc-acbbc13cfcfd">WS_XML_READER</a> object and the referenced <b>Reader</b> value may not be <b>NULL</b>.
        


### -param moveTo [in]

This enumerator specifies direction or next position of the Reader relative to the current position.


### -param found

Indicates success or failure of the specified move.


### -param error [in, optional]

A  pointer to a <a href="https://msdn.microsoft.com/d5763d93-8eff-4df8-9a8a-a58aefabcb21">WS_ERROR</a> object where additional information about the error should be stored if the function fails.
                


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
<dt><b>WS_E_INVALID_OPERATION</b></dt>
</dl>
</td>
<td width="60%">
The operation is not allowed due to the current state of the object.

</td>
</tr>
</table>
 




## -remarks



If the found parameter is not <b>NULL</b>, then it will indicate there whether or not it could
        move to the requested node and return NOERROR.
      

If the found parameter is <b>NULL</b>, and the requested node is not found, it will return <b>WS_E_INVALID_FORMAT</b>.
      (See <a href="https://msdn.microsoft.com/96285557-8317-4875-b634-e2eacd605901">Windows Web Services Return Values</a>.) 

This function cannot be used while canonicalizing.  If <a href="https://msdn.microsoft.com/5dad9485-db3c-4ae0-b053-e1e4f32ad64d">WsStartReaderCanonicalization</a> has
        been called, then it will return <b>WS_E_INVALID_OPERATION</b>.
      



