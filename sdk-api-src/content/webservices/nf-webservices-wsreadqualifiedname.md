---
UID: NF:webservices.WsReadQualifiedName
title: WsReadQualifiedName function
author: windows-sdk-content
description: Reads a qualified name and separates it into its prefix, localName and namespace based on the current namespace scope of the XML_READER.
old-location: wsw\wsreadqualifiedname.htm
tech.root: wsw
ms.assetid: bc49fb89-72ba-435a-ac50-303f16d36da2
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: WsReadQualifiedName, WsReadQualifiedName function [Web Services for Windows], webservices/WsReadQualifiedName, wsw.wsreadqualifiedname
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
 - WsReadQualifiedName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WsReadQualifiedName function


## -description


Reads a qualified name and separates it into its prefix, localName 
        and namespace based on the current namespace scope of the XML_READER. 
        If the ns parameter is specified, then the namespace that the prefix 
        is bound to will be returned, or <b>WS_E_INVALID_FORMAT</b>will be returned. (See <a href="https://msdn.microsoft.com/96285557-8317-4875-b634-e2eacd605901">Windows Web Services Return Values</a>.) The strings are placed in the specified heap.
      


## -parameters




### -param reader [in]

The reader which should read the qualified name.
        


### -param heap [in]

The heap on which the resulting strings should be allocated.
        


### -param prefix

The prefix of the qualified name is returned here.
        


### -param localName [out]

The localName of the qualified name is returned here.
        


### -param ns

The namespace to which the qualified name is bound is returned here.
        


### -param error [in, optional]

If the localName is missing the function will return <b>WS_E_INVALID_FORMAT</b>.  
          If the ns parameter is specified, but the prefix is not bound to a namespace, 
           <b>WS_E_INVALID_FORMAT</b> will be returned.
        


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
</table>
 



