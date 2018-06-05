---
UID: NF:wdstci.WdsTransportClientAddRefBuffer
title: WdsTransportClientAddRefBuffer function
author: windows-sdk-content
description: Increments the reference count on a buffer owned by the multicast client.
old-location: wds\wdstransportclientaddrefbuffer.htm
old-project: Wds
ms.assetid: 941cac20-cca9-4351-8dee-f3910062c6b4
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: WdsTransportClientAddRefBuffer, WdsTransportClientAddRefBuffer function [Windows Deployment Services], wds.wdstransportclientaddrefbuffer, wdstci/WdsTransportClientAddRefBuffer
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: TRANSPORTCLIENT_CALLBACK_ID, *PTRANSPORTCLIENT_CALLBACK_ID
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Wdstptc.dll
api_name:
-	WdsTransportClientAddRefBuffer
product: Windows
targetos: Windows
req.lib: Wdstptc.lib
req.dll: Wdstptc.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WdsTransportClientAddRefBuffer function


## -description


Increments the reference count on a buffer owned by the multicast client.


## -parameters




### -param pvBuffer [in]

The buffer on which to increment the reference count.


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.



