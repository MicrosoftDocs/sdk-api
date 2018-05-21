---
UID: NF:webservices.WsRevokeSecurityContext
title: WsRevokeSecurityContext function
author: windows-driver-content
description: Revokes a security context.
old-location: wsw\wsrevokesecuritycontext.htm
old-project: wsw
ms.assetid: 07367f3d-4158-4ef4-ac27-4218d2a810a8
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: WsRevokeSecurityContext, WsRevokeSecurityContext function [Web Services for Windows], webservices/WsRevokeSecurityContext, wsw.wsrevokesecuritycontext
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
-	WsRevokeSecurityContext
product: Windows
targetos: Windows
req.lib: WebServices.lib
req.dll: WebServices.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WsRevokeSecurityContext function


## -description



        Revokes a security context. Can only be called on the server side. 
        Further requests using this security context will fail and a fault will be sent to the client.
      


        This function can be used when the server knows that no more messages are 
        coming and does not want to wait for the client or the context timeouts to 
        trigger the reclaiming of resources, or when the server wants to engage in 
        active context management.
      


## -parameters




### -param securityContext [in]


          The security context to be revoked.
        


### -param error [in, optional]


          Specifies where additional error information should be stored if the function fails.
        


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



