---
UID: NF:webservices.WsXmlStringEquals
title: WsXmlStringEquals function
author: windows-sdk-content
description: Compares two WS_XML_STRING objects for equality. The operation performs an ordinal comparison of the character values contained by the String objects.
old-location: wsw\wsxmlstringequals.htm
tech.root: wsw
ms.assetid: 4fcff6d7-b17c-4cd6-9671-1aff7b84fa98
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: WsXmlStringEquals, WsXmlStringEquals function [Web Services for Windows], webservices/WsXmlStringEquals, wsw.wsxmlstringequals
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
 - WsXmlStringEquals
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WsXmlStringEquals function


## -description


Compares two <a href="https://msdn.microsoft.com/3daa656f-7f97-4e29-a556-7ff72206f01c">WS_XML_STRING</a> objects for equality.  The operation performs an ordinal comparison
        of the character values contained by the String objects.
      


## -parameters




### -param string1 [in]

A pointer to the first string to compare.
        


### -param string2 [in]

A pointer to the second string to compare.
        


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
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The strings are equal.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The strings are not equal.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are not correct.

</td>
</tr>
</table>
 




## -remarks



This function is typically used to compare localNames and namespaces in XML.  



