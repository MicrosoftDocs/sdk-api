---
UID: NF:wsddisco.WSDCreateDiscoveryProvider2
title: WSDCreateDiscoveryProvider2 function
author: windows-sdk-content
description: Creates an IWSDiscoveryProvider object that supports signed messages.
old-location: ncd\wsdcreatediscoveryprovider2.htm
old-project: WsdApi
ms.assetid: dc757897-032c-4ea3-8f4e-cf00d4ec385b
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: WSDCreateDiscoveryProvider2, WSDCreateDiscoveryProvider2 function, ncd.wsdcreatediscoveryprovider2, wsddisco/WSDCreateDiscoveryProvider2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wsddisco.h
req.include-header: Wsdapi.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: WSD_SECURITY_SIGNATURE_VALIDATION, *PWSD_SECURITY_SIGNATURE_VALIDATION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wsdapi.dll
api_name:
 - WSDCreateDiscoveryProvider2
product: Windows
targetos: Windows
req.lib: Wsdapi.lib
req.dll: Wsdapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WSDCreateDiscoveryProvider2 function


## -description


Creates an <a href="https://msdn.microsoft.com/e3d3acc2-914b-40bd-9e1e-a3a612821ab7">IWSDiscoveryProvider</a> object that supports signed messages.


## -parameters




### -param pContext [in]

An <a href="https://msdn.microsoft.com/131fa170-4c19-4a7b-82e0-e9677b7f767a">IWSDXMLContext</a> interface that defines custom message types or namespaces.

If <b>NULL</b>, a default context representing the built-in message types and namespaces is used.


### -param pConfigParams [in]

An array of <a href="https://msdn.microsoft.com/58dc3e11-586e-4185-b1d0-4249b4bfb252">WSD_CONFIG_PARAM</a> structures that contain the parameters for creating the object.


### -param dwConfigParamCount [in]

The total number of structures passed in <i>pConfigParams</i>.


### -param ppProvider [out]

Returns a reference to the initialized <a href="https://msdn.microsoft.com/e3d3acc2-914b-40bd-9e1e-a3a612821ab7">IWSDiscoveryProvider</a> object. Cannot be <b>NULL</b>.


## -returns



Possible return values include, but are not limited to, the following:

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
Function completed successfully.

</td>
</tr>
</table>
 



