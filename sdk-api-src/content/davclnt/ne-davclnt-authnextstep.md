---
UID: NE:davclnt.AUTHNEXTSTEP
title: AUTHNEXTSTEP
author: windows-sdk-content
description: Specifies the next action that the WebDAV client should take after a successful call to the DavAuthCallback callback function.
old-location: webdav\authnextstep.htm
old-project: webdav
ms.assetid: e9ce9e61-c395-4f6b-843c-c1caa13ac3b4
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: AUTHNEXTSTEP, AUTHNEXTSTEP enumeration [WebDAV], CancelRequest, DefaultBehavior, RetryRequest, davclnt/AUTHNEXTSTEP, davclnt/CancelRequest, davclnt/DefaultBehavior, davclnt/RetryRequest, webdav.authnextstep
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: davclnt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 with SP2 [desktop apps only]
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
req.typenames: AUTHNEXTSTEP
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - davclnt.h
api_name:
 - AUTHNEXTSTEP
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# AUTHNEXTSTEP enumeration


## -description


Specifies the next action that the WebDAV client should take after  a successful call to the <a href="https://msdn.microsoft.com/6ac191ac-e63f-431f-893b-92c69320db58">DavAuthCallback</a> callback function.


## -enum-fields




### -field DefaultBehavior

Retry the connection request without using the <a href="https://msdn.microsoft.com/6ac191ac-e63f-431f-893b-92c69320db58">DavAuthCallback</a> callback function. This is the same as the default behavior if no callback function is registered.


### -field RetryRequest

Retry the connection request using the credentials that were retrieved by the <a href="https://msdn.microsoft.com/6ac191ac-e63f-431f-893b-92c69320db58">DavAuthCallback</a> function.


### -field CancelRequest

Cancel the connection request.


## -remarks



This enumeration provides the values for the <i>NextStep</i> parameter of the <a href="https://msdn.microsoft.com/6ac191ac-e63f-431f-893b-92c69320db58">DavAuthCallback</a> callback function.



