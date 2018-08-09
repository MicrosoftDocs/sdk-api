---
UID: NF:wdstci.WdsTransportClientReleaseBuffer
title: WdsTransportClientReleaseBuffer function
author: windows-sdk-content
description: Decrements the reference count on a buffer owned by the multicast client.
old-location: wds\wdstransportclientreleasebuffer.htm
old-project: wds
ms.assetid: bf0dcb89-0bc2-4e93-94ce-5c50039ef22b
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: WdsTransportClientReleaseBuffer, WdsTransportClientReleaseBuffer function [Windows Deployment Services], wds.wdstransportclientreleasebuffer, wdstci/WdsTransportClientReleaseBuffer
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
 - WdsTransportClientReleaseBuffer
product: Windows
targetos: Windows
req.lib: Wdstptc.lib
req.dll: Wdstptc.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WdsTransportClientReleaseBuffer function


## -description


Decrements the reference count on a buffer owned by the multicast client.


## -parameters




### -param pvBuffer [in]

The buffer on which to decrement the reference count.


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.



