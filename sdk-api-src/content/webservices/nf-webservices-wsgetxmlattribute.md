---
UID: NF:webservices.WsGetXmlAttribute
title: WsGetXmlAttribute function (webservices.h)
description: Finds the nearest xml attribute in scope with the specified localName and returns its value. The returned value is placed on the specified heap.
helpviewer_keywords: ["WsGetXmlAttribute","WsGetXmlAttribute function [Web Services for Windows]","webservices/WsGetXmlAttribute","wsw.wsgetxmlattribute"]
old-location: wsw\wsgetxmlattribute.htm
tech.root: wsw
ms.assetid: dca29f9b-a218-4764-bf7e-98a027c4336d
ms.date: 12/05/2018
ms.keywords: WsGetXmlAttribute, WsGetXmlAttribute function [Web Services for Windows], webservices/WsGetXmlAttribute, wsw.wsgetxmlattribute
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WsGetXmlAttribute
 - webservices/WsGetXmlAttribute
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WebServices.dll
api_name:
 - WsGetXmlAttribute
---

# WsGetXmlAttribute function


## -description

Finds the nearest xml attribute in scope with the specified localName and returns its value.  
        The returned value is placed on the specified heap.

## -parameters

### -param reader [in]

The reader for which the xml attribute will be searched.

### -param localName [in]

The localName of the xml attribute for which to search.

### -param heap [in]

The heap on which the resulting value should be allocated.

### -param valueChars

The value of the attribute is stored here.

### -param valueCharCount [out]

The length of the valueChars.

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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The xml attribute was not found.
      

</td>
</tr>
</table>

## -remarks

This function may only be used to obtain the values of attributes in scope that use the prefix "xml".
      

If no matching xml attribute is found, a zero length string will be returned for the value, and the
        function returns S_FALSE.
      

The reader does not do anything with xml attributes other than to surface them for inspection.

