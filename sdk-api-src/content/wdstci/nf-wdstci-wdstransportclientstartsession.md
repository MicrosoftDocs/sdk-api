---
UID: NF:wdstci.WdsTransportClientStartSession
title: WdsTransportClientStartSession function
author: windows-sdk-content
description: Initiates a multicast file transfer.
old-location: wds\wdstransportclientstartsession.htm
tech.root: Wds
ms.assetid: aa89899f-8f50-4617-84a1-4013412f0292
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: WdsTransportClientStartSession, WdsTransportClientStartSession function [Windows Deployment Services], wds.wdstransportclientstartsession, wdstci/WdsTransportClientStartSession
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
 - WdsTransportClientStartSession
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WdsTransportClientStartSession function


## -description


Initiates a multicast file transfer.


## -parameters




### -param hSessionKey [in]

The handle returned by the <a href="https://msdn.microsoft.com/0ece4ac8-372c-46ec-a6a1-ff1b547a85ef">WdsTransportClientInitializeSession</a> session.


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.




## -remarks



All callbacks must be registered before this function is called.  If a required callback is not registered, this function will fail.

It is possible for a session to start and complete before this function  returns. This means that it is possible to receive a callback with a session handle that has not been seen yet.  This also means that a session can start and error out before this function has a chance to complete.  In this case, this function may still return success, even if the session itself fails.



