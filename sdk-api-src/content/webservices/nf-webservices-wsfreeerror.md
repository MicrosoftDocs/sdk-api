---
UID: NF:webservices.WsFreeError
title: WsFreeError function
author: windows-sdk-content
description: Releases the memory resource associated with an Error object created using WsCreateError. This releases the object and its constituent information.
old-location: wsw\wsfreeerror.htm
old-project: wsw
ms.assetid: 61da7bc2-b805-4379-a6b2-1e92374be1a0
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: WsFreeError, WsFreeError function [Web Services for Windows], webservices/WsFreeError, wsw.wsfreeerror
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
 - WsFreeError
product: Windows
targetos: Windows
req.lib: WebServices.lib
req.dll: WebServices.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WsFreeError function


## -description


Releases the memory resource associated with an   <b>Error</b> object created using  <a href="https://msdn.microsoft.com/0ec858f7-12a5-43cf-94a7-3838ab6d76ae">WsCreateError</a>.
            This releases the object and its constituent information.
            


## -parameters




### -param error [in]


                    A pointer to the <b>Error</b> object to release.  The pointer must reference a valid <b>WS_ERROR</b> object
                    returned by <a href="https://msdn.microsoft.com/0ec858f7-12a5-43cf-94a7-3838ab6d76ae">WsCreateError</a>.  The referenced value may 
                    not be NULL.
                


## -returns



This function does not return a value.



