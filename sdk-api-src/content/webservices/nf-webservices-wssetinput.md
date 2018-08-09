---
UID: NF:webservices.WsSetInput
title: WsSetInput function
author: windows-sdk-content
description: Sets the encoding and input sources for an XML Reader.
old-location: wsw\wssetinput.htm
old-project: wsw
ms.assetid: d7ac5233-266e-4ca1-aa58-e50b385b48bb
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: WsSetInput, WsSetInput function [Web Services for Windows], webservices/WsSetInput, wsw.wssetinput
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
 - WsSetInput
product: Windows
targetos: Windows
req.lib: WebServices.lib
req.dll: WebServices.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WsSetInput function


## -description


Sets the encoding and input sources for an XML  Reader.
      These settings override settings made when the Reader was created.<div class="alert"><b>Note</b>  If both encoding and input are <b>NULL</b> the reader will operate as if it is positioned at the end of an empty XML document.
      </div>
<div> </div>



## -parameters




### -param reader [in]

A pointer to the <a href="https://msdn.microsoft.com/7acbe407-e91b-435a-82bc-acbbc13cfcfd">WS_XML_READER</a> object for which the input will be set.
        


### -param encoding [in, optional]

A to an encoding value that describes the format of the input bytes.  This value should be one of:<ul>
<li>
<a href="https://msdn.microsoft.com/ffb351d7-36dc-44ce-8a5e-ee452ca8b4e6">WS_XML_READER_TEXT_ENCODING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/51a0802b-6624-430e-96c1-a8470fac4937">WS_XML_READER_BINARY_ENCODING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/dec4d9ad-71d3-48f9-b6c3-49cf6bcb85fb">WS_XML_READER_MTOM_ENCODING</a>
</li>
</ul>



### -param input [in, optional]

A pointer to a <a href="https://msdn.microsoft.com/1e7a708d-5dcf-44ec-b781-a34946cb2844">WS_XML_READER_INPUT</a> structure that indicates the reader type.


### -param properties

An array reference of optional Reader properties.  


### -param propertyCount [in]

The number of properties.


### -param error [in, optional]

A  pointer to a <a href="https://msdn.microsoft.com/d5763d93-8eff-4df8-9a8a-a58aefabcb21">WS_ERROR</a> object where additional information about the error should be stored if the function fails.
                


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



When <b>WsSetInput</b> is used on the XML Reader, the reader will function in a forward only manner and
        the functions <a href="https://msdn.microsoft.com/91e543f3-7325-4a90-9b99-c98918478853">WsGetReaderPosition</a>, <a href="https://msdn.microsoft.com/cc879cc0-c8ca-457e-9ff1-ae220e31cb04">WsSetReaderPosition</a> and <a href="https://msdn.microsoft.com/63d18407-f82b-4884-a162-2c8163e883e1">WsMoveReader</a> cannot be used.
      





