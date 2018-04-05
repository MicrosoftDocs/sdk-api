---
UID: NF:webservices.WsFreeServiceHost
title: WsFreeServiceHost function
author: windows-driver-content
description: Releases the memory associated with a Service Host object.
old-location: wsw\wsfreeservicehost.htm
old-project: wsw
ms.assetid: 5362d8a4-8b38-462a-a7c1-9cde19abee1e
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: WsFreeServiceHost, WsFreeServiceHost function [Web Services for Windows], webservices/WsFreeServiceHost, wsw.wsfreeservicehost
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: webservices.h
req.include-header: 
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
req.typenames: WS_SECURITY_ALGORITHM_PROPERTY_ID
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	WebServices.dll
api_name:
-	WsFreeServiceHost
product: Windows
targetos: Windows
req.lib: WebServices.lib
req.dll: WebServices.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WsFreeServiceHost function


## -description


Releases the memory associated with  a <a href="https://msdn.microsoft.com/42e4d24d-5611-4561-b874-6dc3f3f88c73">Service Host</a> object.
            


## -parameters




### -param serviceHost [in]

A pointer to the <b>Service Host</b> object to release.  The pointer must reference a valid <a href="https://msdn.microsoft.com/1186e3ae-87d0-4d0b-a7cc-cce63dc091e2">WS_SERVICE_HOST</a> object
                    returned by <a href="https://msdn.microsoft.com/412a262a-1706-4101-b154-1804408a5b9f">WsCreateServiceHost</a> and the referenced <b>Service Host</b> value may not be <b>NULL</b>.
        
                


## -returns



This function does not return a value.



