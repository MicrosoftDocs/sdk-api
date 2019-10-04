---
UID: NF:webservices.WsGetDictionary
title: WsGetDictionary function (webservices.h)
author: windows-sdk-content
description: Retrieves an XML Dictionary object. The retrieved Dictionary is returned by the dictionary reference parameter.
old-location: wsw\wsgetdictionary.htm
tech.root: wsw
ms.assetid: 85736dc0-671b-463f-b7ba-458cdd9001fc
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WsGetDictionary, WsGetDictionary function [Web Services for Windows], webservices/WsGetDictionary, wsw.wsgetdictionary
ms.topic: function
f1_keywords:
- webservices/WsGetDictionary
dev_langs:
 - c++
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
- WsGetDictionary
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# WsGetDictionary function


## -description


Retrieves an <a href="https://docs.microsoft.com/windows/desktop/api/webservices/ns-webservices-ws_xml_dictionary">XML Dictionary</a> object. The retrieved Dictionary is returned by the <i>dictionary</i> reference parameter.


## -parameters




### -param encoding [in]

Indicates an enumeration of the Dictionary encoding.
        


### -param dictionary

A reference to a <a href="https://docs.microsoft.com/windows/desktop/api/webservices/ns-webservices-ws_xml_dictionary">WS_XML_DICTIONARY</a> structure for the retrieved <b>Dictionary</b>.
        


### -param error [in, optional]

A  pointer to a <a href="https://docs.microsoft.com/windows/desktop/wsw/ws-error">WS_ERROR</a> object where additional information about the error should be stored if the function fails.
                


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



