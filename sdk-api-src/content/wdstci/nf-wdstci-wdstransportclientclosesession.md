---
UID: NF:wdstci.WdsTransportClientCloseSession
title: WdsTransportClientCloseSession function
author: windows-sdk-content
description: Releases the resources associated with a session in the client.
old-location: wds\wdstransportclientclosesession.htm
tech.root: wds
ms.assetid: 4c135502-a6be-4d5d-b6ce-34b55f6e08b0
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: WdsTransportClientCloseSession, WdsTransportClientCloseSession function [Windows Deployment Services], wds.wdstransportclientclosesession, wdstci/WdsTransportClientCloseSession
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wdstci.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP1 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wdstptc.lib
req.dll: Wdstptc.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wdstptc.dll
api_name:
 - WdsTransportClientCloseSession
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- WdsTransportClientCloseSession
: 
---

# WdsTransportClientCloseSession function


## -description


Releases the resources associated with a session in the client.


## -parameters




### -param hSessionKey [in]

Unique handle returned by the call to <a href="https://msdn.microsoft.com/0ece4ac8-372c-46ec-a6a1-ff1b547a85ef">WdsTransportClientInitializeSession</a>. After this handle has been used with the <b>WdsTransportClientCloseSession</b>, it cannot be used again with the <a href="https://msdn.microsoft.com/96348bbf-e1b6-4889-a2a6-59d265c1a031">WdsTransportClientCancelSession</a> function. 


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.




## -remarks



This function does not cancel the session and callbacks  can be received until session completes. 



