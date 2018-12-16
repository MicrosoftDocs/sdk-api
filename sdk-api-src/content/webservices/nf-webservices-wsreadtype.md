---
UID: NF:webservices.WsReadType
title: WsReadType function
author: windows-sdk-content
description: Read a value of a given WS_TYPE from XML according to the WS_TYPE_MAPPING.
old-location: wsw\wsreadtype.htm
tech.root: wsw
ms.assetid: 6d026b2e-f2c2-4990-9178-152585a7749a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WsReadType, WsReadType function [Web Services for Windows], webservices/WsReadType, wsw.wsreadtype
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
 - WsReadType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WsReadType function


## -description


Read a value of a given <a href="https://msdn.microsoft.com/en-us/library/Dd323479(v=VS.85).aspx">WS_TYPE</a> from XML according to the <a href="https://msdn.microsoft.com/en-us/library/Dd323480(v=VS.85).aspx">WS_TYPE_MAPPING</a>.
            


## -parameters




### -param reader [in]

The reader that is positioned on the XML to deserialize.
                


### -param typeMapping [in]

Describes how the type maps to the XML that is being read.
                


### -param type [in]

The type of the value to deserialize.
                


### -param typeDescription [in, optional]

Additional information about the type.  Each type has a different description
                    structure.  This may be <b>NULL</b>, depending on the <a href="https://msdn.microsoft.com/en-us/library/Dd323479(v=VS.85).aspx">WS_TYPE</a>.
                


### -param readOption [in]

Whether the value is required, and how to allocate the value.
                    See <a href="https://msdn.microsoft.com/en-us/library/Dd402008(v=VS.85).aspx">WS_READ_OPTION</a> for more information.
                

This parameter must have one of the following values:
                

<ul>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Dd402008(v=VS.85).aspx">WS_READ_REQUIRED_VALUE</a>.
                    </li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Dd402008(v=VS.85).aspx">WS_READ_REQUIRED_POINTER</a>.
                </li>
</ul>

### -param heap [in, optional]

The heap to store the deserialized values in.
                


### -param value

The interpretation of this parameter depends on the <a href="https://msdn.microsoft.com/en-us/library/Dd402008(v=VS.85).aspx">WS_READ_OPTION</a>.
                


### -param valueSize [in]

The interpretation of this parameter depends on the <a href="https://msdn.microsoft.com/en-us/library/Dd402008(v=VS.85).aspx">WS_READ_OPTION</a>.
                


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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Ran out of memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_QUOTA_EXCEEDED</b></dt>
</dl>
</td>
<td width="60%">
The size quota of the heap was exceeded.
                

</td>
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



See <a href="https://msdn.microsoft.com/en-us/library/Dd323480(v=VS.85).aspx">WS_TYPE_MAPPING</a> for how to use this function to read values from elements and attributes.
            

If the API fails, the state of input reader becomes undefined. The only APIs that may be used on the reader
        if this occurs are <a href="https://msdn.microsoft.com/d7ac5233-266e-4ca1-aa58-e50b385b48bb">WsSetInput</a> and <a href="https://msdn.microsoft.com/0b3ac6ab-8c16-4189-950d-84bdcdabcde0">WsSetInputToBuffer</a> to return the reader to a usable state,
        or <a href="https://msdn.microsoft.com/31163bea-266f-43a3-bdf5-61386ebc197c">WsFreeReader</a> to free the reader.
            



