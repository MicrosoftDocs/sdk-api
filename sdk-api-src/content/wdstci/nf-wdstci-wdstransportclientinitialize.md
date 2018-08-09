---
UID: NF:wdstci.WdsTransportClientInitialize
title: WdsTransportClientInitialize function
author: windows-sdk-content
description: Initializes the Multicast Client.
old-location: wds\wdstransportclientinitialize.htm
old-project: wds
ms.assetid: 6494a155-61de-40bd-a29a-79134da96bbe
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: WdsTransportClientInitialize, WdsTransportClientInitialize function [Windows Deployment Services], wds.wdstransportclientinitialize, wdstci/WdsTransportClientInitialize
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
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wdstptc.dll
api_name:
 - WdsTransportClientInitialize
product: Windows
targetos: Windows
req.lib: Wdstptc.lib
req.dll: Wdstptc.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WdsTransportClientInitialize function


## -description


Initializes the Multicast Client. This function should be called before any other function is called in the multicast client. 


## -parameters






## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.



