---
UID: NS:wsman._WSMAN_PROXY_INFO
title: WSMAN_PROXY_INFO
author: windows-sdk-content
description: Specifies proxy information.
old-location: winrm\wsman_proxy_info.htm
tech.root: winrm
ms.assetid: 0542fa39-c574-4a5e-b8eb-6ddf8a58600a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WSMAN_PROXY_INFO, WSMAN_PROXY_INFO structure [Windows Remote Management], winrm.wsman_proxy_info, wsman/WSMAN_PROXY_INFO
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: wsman.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
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
 - Wsman.h
api_name:
 - WSMAN_PROXY_INFO
product: Windows
targetos: Windows
req.typenames: WSMAN_PROXY_INFO
req.redist: Windows Management Framework on Windows Server 2008 with SP2, Windows Vista with SP1, and Windows Vista with SP2
---

# WSMAN_PROXY_INFO structure


## -description


Specifies proxy information.


## -struct-fields




### -field accessType

Specifies the access type for the proxy. This member must be set to one of the values defined in the <a href="https://msdn.microsoft.com/0c7d13dc-42e0-4c91-bcdf-c198b557206b">WSManProxyAccessType</a> enumeration.


### -field authenticationCredentials

A <a href="https://msdn.microsoft.com/e9090d88-c76e-4a85-946e-ff46403e6725">WSMAN_AUTHENTICATION_CREDENTIALS</a> structure that specifies the credentials and authentication scheme used for proxy access.

