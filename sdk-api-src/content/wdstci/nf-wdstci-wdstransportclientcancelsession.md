---
UID: NF:wdstci.WdsTransportClientCancelSession
title: WdsTransportClientCancelSession function
author: windows-sdk-content
description: Releases the resources associated with a session in the client.
old-location: wds\wdstransportclientcancelsession.htm
tech.root: wds
ms.assetid: 96348bbf-e1b6-4889-a2a6-59d265c1a031
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: WdsTransportClientCancelSession, WdsTransportClientCancelSession function [Windows Deployment Services], wds.wdstransportclientcancelsession, wdstci/WdsTransportClientCancelSession
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
 - WdsTransportClientCancelSession
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- WdsTransportClientCancelSession
: 
---

# WdsTransportClientCancelSession function


## -description


Releases the resources associated with a session in the client.


## -parameters




### -param hSessionKey [in]

Unique handle returned by the call to <a href="https://msdn.microsoft.com/0ece4ac8-372c-46ec-a6a1-ff1b547a85ef">WdsTransportClientInitializeSession</a>.  This session will eventually complete with an error code of <b>ERROR_CANCELLED</b> to the callback <a href="https://msdn.microsoft.com/1c7b8137-bf74-486c-a90e-6becfec5ddc8">PFN_WdsTransportClientSessionComplete</a> callback.


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.




## -remarks



It is safe to call this function from within a callback.



