---
UID: NF:wdstci.WdsTransportClientWaitForCompletion
title: WdsTransportClientWaitForCompletion function
author: windows-driver-content
description: Blocks until either the multicast session is complete or the specified timeout is reached.
old-location: wds\wdstransportclientwaitforcompletion.htm
old-project: Wds
ms.assetid: b592ae66-5090-468e-a747-346f87e807e8
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: WdsTransportClientWaitForCompletion, WdsTransportClientWaitForCompletion function [Windows Deployment Services], wds.wdstransportclientwaitforcompletion, wdstci/WdsTransportClientWaitForCompletion
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
req.typenames: TRANSPORTCLIENT_CALLBACK_ID, *PTRANSPORTCLIENT_CALLBACK_ID
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Wdstptc.dll
api_name:
-	WdsTransportClientWaitForCompletion
product: Windows
targetos: Windows
req.lib: Wdstptc.lib
req.dll: Wdstptc.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WdsTransportClientWaitForCompletion function


## -description


Blocks until either the multicast session is complete or the specified timeout is reached.


## -parameters




### -param hSessionKey [in]

Unique handle returned by the call to <a href="https://msdn.microsoft.com/0ece4ac8-372c-46ec-a6a1-ff1b547a85ef">WdsTransportClientInitializeSession</a>.


### -param uTimeout [in]

A timeout, in milliseconds.


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.



