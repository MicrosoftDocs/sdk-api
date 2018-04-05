---
UID: NF:webservices.WsFreeWriter
title: WsFreeWriter function
author: windows-driver-content
description: Releases the memory resource associated with an XML Writer object.
old-location: wsw\wsfreewriter.htm
old-project: wsw
ms.assetid: eb1eb835-838a-41e4-9e7d-c5c805237f65
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: WsFreeWriter, WsFreeWriter function [Web Services for Windows], webservices/WsFreeWriter, wsw.wsfreewriter
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: WS_SECURITY_ALGORITHM_PROPERTY_ID
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	WebServices.dll
api_name:
-	WsFreeWriter
product: Windows
targetos: Windows
req.lib: WebServices.lib
req.dll: WebServices.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WsFreeWriter function


## -description


Releases the memory resource associated with  an  XML Writer object.
            


## -parameters




### -param writer [in]

A pointer to the <b>XML Writer</b> object to release.  The pointer must reference a valid <a href="https://msdn.microsoft.com/8f413e60-8a30-492c-8f2d-80be511fee11">WS_XML_WRITER</a> object
                    returned by <a href="https://msdn.microsoft.com/5b4bb009-764e-4892-903a-5939f5570016">WsCreateWriter</a> and   the referenced value may not be <b>NULL</b>.
                


## -returns



This function does not return a value.




## -remarks




        If necessary, <a href="https://msdn.microsoft.com/ba631942-d5a0-4d93-9899-c3f0ebd4aae5">WsFlushWriter</a> should be called before calling <b>WsFreeWriter</b> to guarantee
        all data is emitted.
      



