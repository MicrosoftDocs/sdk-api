---
UID: NF:wdstci.WdsTransportClientCompleteReceive
title: WdsTransportClientCompleteReceive function
author: windows-sdk-content
description: Indicates that all processing on a block of data is finished, and that the multicast client may purge this block of data from its cache to make room for further receives.
old-location: wds\wdstransportclientcompletereceive.htm
old-project: Wds
ms.assetid: 1c5cdd44-e818-43ef-aaba-60a01660f7cf
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: WdsTransportClientCompleteReceive, WdsTransportClientCompleteReceive function [Windows Deployment Services], wds.wdstransportclientcompletereceive, wdstci/WdsTransportClientCompleteReceive
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
 - WdsTransportClientCompleteReceive
product: Windows
targetos: Windows
req.lib: Wdstptc.lib
req.dll: Wdstptc.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WdsTransportClientCompleteReceive function


## -description


Indicates that all processing on a block of data is finished, and that the multicast client may purge this block of data from its cache to make room for further receives.


## -parameters




### -param hSessionKey [in]

Unique handle returned by the call to <a href="https://msdn.microsoft.com/0ece4ac8-372c-46ec-a6a1-ff1b547a85ef">WdsTransportClientInitializeSession</a>.


### -param ulSize [in]

The size of the block being released.


### -param pullOffset [in]

The offset of the block being released.


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.




## -remarks



There must be one call to <b>WdsTransportClientCompleteReceive</b> for each call to the <a href="https://msdn.microsoft.com/3a1cd9bb-c0da-4d66-9338-1f284fc15499">PFN_WdsTransportClientReceiveContents</a> callback that the consumer receives.  The length and offset parameters of this function call must match those provided in the receive contents callback.  Failure to call this function will result in a stall in the multicast client once it hits the cache limit specified by the <i>ulCacheSize</i> of the <a href="https://msdn.microsoft.com/efa1ea12-5234-474b-a859-cd074290e375">WDS_TRANSPORTCLIENT_REQUEST</a> structure passed to <a href="https://msdn.microsoft.com/0ece4ac8-372c-46ec-a6a1-ff1b547a85ef">WdsTransportClientInitializeSession</a>.



