---
UID: NF:webservices.WsFreeSecurityToken
title: WsFreeSecurityToken function
author: windows-sdk-content
description: Releases the memory resource associated with a Security Token object.
old-location: wsw\wsfreesecuritytoken.htm
tech.root: wsw
ms.assetid: 7f9500a8-b54f-4967-8f8d-9f8770d3dd60
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: WsFreeSecurityToken, WsFreeSecurityToken function [Web Services for Windows], webservices/WsFreeSecurityToken, wsw.wsfreesecuritytoken
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
 - WsFreeSecurityToken
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WsFreeSecurityToken function


## -description


Releases the memory resource associated with  a <b>Security Token</b> object.
            


## -parameters




### -param token [in]

A pointer to the <b>Security Token</b> object to release.  The pointer must reference a valid <a href="https://msdn.microsoft.com/050a2ce5-279e-48fb-85da-1d0b11cd8229">WS_SECURITY_TOKEN</a>object returned by <a href="https://msdn.microsoft.com/1d82c6c3-2bcf-4883-aed7-1a163bbb2228">WsCreateXmlSecurityToken</a>.
                


## -returns



This function does not return a value.



