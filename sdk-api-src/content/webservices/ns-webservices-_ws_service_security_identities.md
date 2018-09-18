---
UID: NS:webservices._WS_SERVICE_SECURITY_IDENTITIES
title: "_WS_SERVICE_SECURITY_IDENTITIES"
author: windows-sdk-content
description: A list of Server Principal Names (SPNs) that are used to validate Extended Protection.
old-location: wsw\ws_service_security_identities.htm
tech.root: wsw
ms.assetid: d38f0efd-2570-4db1-b4f7-113a45fe4449
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: WS_SERVICE_SECURITY_IDENTITIES, WS_SERVICE_SECURITY_IDENTITIES structure [Web Services for Windows], _WS_SERVICE_SECURITY_IDENTITIES, webservices/WS_SERVICE_SECURITY_IDENTITIES, wsw.ws_service_security_identities
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: v.1.0
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WebServices.h
api_name:
 - WS_SERVICE_SECURITY_IDENTITIES
product: Windows
targetos: Windows
req.typenames: WS_SERVICE_SECURITY_IDENTITIES
req.redist: 
---

# _WS_SERVICE_SECURITY_IDENTITIES structure


## -description


A list of Server Principal Names (SPNs) that are used to validate <a href="https://msdn.microsoft.com/35e48846-05e5-4db9-a3b5-098b62815b66">Extended Protection</a>. 
            

Only available on the server.
            


## -struct-fields




### -field serviceIdentities

A array of strings representing the SPNs accepted by the server. Wildcards are not allowed.
                


### -field serviceIdentityCount

The number of strings in serviceIdentities.
                

