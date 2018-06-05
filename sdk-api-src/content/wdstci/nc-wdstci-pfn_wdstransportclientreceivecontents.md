---
UID: NC:wdstci.PFN_WdsTransportClientReceiveContents
title: PFN_WdsTransportClientReceiveContents
author: windows-sdk-content
description: The PFN_WdsTransportClientReceiveContents callback is used by the multicast client to indicate that a block of data is ready to be used.
old-location: wds\pfn_wdstransportclientreceivecontents.htm
old-project: Wds
ms.assetid: 3a1cd9bb-c0da-4d66-9338-1f284fc15499
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: PFN_WdsTransportClientReceiveContents, PFN_WdsTransportClientReceiveContents callback, PFN_WdsTransportClientReceiveContents callback function [Windows Deployment Services], wds.pfn_wdstransportclientreceivecontents, wdstci/PFN_WdsTransportClientReceiveContents
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
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
req.typenames: PXE_PROVIDER, *PPXE_PROVIDER
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	Wdstci.h
api_name:
-	PFN_WdsTransportClientReceiveContents
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# PFN_WdsTransportClientReceiveContents callback function


## -description


The PFN_WdsTransportClientReceiveContents callback is used by the multicast client to indicate that a block of data is ready to be used.


## -parameters




### -param hSessionKey [in]

The handle belonging to the session that is being started.


### -param pCallerData [in]

Pointer to the user data for this session.  This data was specified in the call to the <a href="https://msdn.microsoft.com/aa89899f-8f50-4617-84a1-4013412f0292">WdsTransportClientStartSession</a> function.


### -param pContents


### -param ulSize [in]

The size of the data in <i>pCallerData</i>.


### -param pullContentOffset








#### - pContentOffset [in]

The offset in the data stream where this block of data starts.  


#### - pMetadata [in]

Pointer to the buffer location  that has received the content. The size of this buffer in bytes is given by <i>ulSize</i>. 


## -returns



This callback function does not return a value.



