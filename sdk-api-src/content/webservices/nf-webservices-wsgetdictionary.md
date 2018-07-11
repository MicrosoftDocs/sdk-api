---
UID: NF:webservices.WsGetDictionary
title: WsGetDictionary function
author: windows-sdk-content
description: Retrieves an XML Dictionary object. The retrieved Dictionary is returned by the dictionary reference parameter.
old-location: wsw\wsgetdictionary.htm
old-project: wsw
ms.assetid: 85736dc0-671b-463f-b7ba-458cdd9001fc
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: WsGetDictionary, WsGetDictionary function [Web Services for Windows], webservices/WsGetDictionary, wsw.wsgetdictionary
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
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WebServices.dll
api_name:
 - WsGetDictionary
product: Windows
targetos: Windows
req.lib: WebServices.lib
req.dll: WebServices.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WsGetDictionary function


## -description


Retrieves an <a href="https://msdn.microsoft.com/2cba47fd-a049-4e50-99dd-20ccf91c9e0f">XML Dictionary</a> object. The retrieved Dictionary is returned by the <i>dictionary</i> reference parameter.


## -parameters




### -param encoding [in]

Indicates an enumeration of the Dictionary encoding.
        


### -param dictionary


            A reference to a <a href="https://msdn.microsoft.com/2cba47fd-a049-4e50-99dd-20ccf91c9e0f">WS_XML_DICTIONARY</a> structure for the retrieved <b>Dictionary</b>.
        


### -param error [in, optional]

A  pointer to a <a href="https://msdn.microsoft.com/d5763d93-8eff-4df8-9a8a-a58aefabcb21">WS_ERROR</a> object where additional information about the error should be stored if the function fails.
                


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



