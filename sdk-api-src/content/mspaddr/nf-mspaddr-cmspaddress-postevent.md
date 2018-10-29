---
UID: NF:mspaddr.CMSPAddress.PostEvent
title: CMSPAddress::PostEvent
author: windows-sdk-content
description: The PostEvent method is called by the MSPCall to post an event to TAPI3. This method puts the event at the end of the event list and signals TAPI3. Locks the event list.
old-location: tapi3\cmspaddress_postevent.htm
tech.root: Tapi
ms.assetid: 25050c11-c270-4fc0-85b4-0f48622a5ec5
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: CMSPAddress interface [TAPI 2.2],PostEvent method, CMSPAddress.PostEvent, CMSPAddress::PostEvent, PostEvent, PostEvent method [TAPI 2.2], PostEvent method [TAPI 2.2],CMSPAddress interface, _tapi3_cmspaddress_postevent, mspaddr/CMSPAddress::PostEvent, tapi3.cmspaddress_postevent
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mspaddr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mspaddr.h
api_name:
 - CMSPAddress.PostEvent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CMSPAddress::PostEvent


## -description


The 
<b>PostEvent</b> method is called by the MSPCall to post an event to TAPI3. This method puts the event at the end of the event list and signals TAPI3. Locks the event list.


## -parameters




### -param EventItem [in]

Pointer to the 
<a href="https://msdn.microsoft.com/fc99fd05-4d87-4b6e-b2f3-e00ac61ddafc">MSPEVENTITEM</a> structure, which contains the event information.


## -see-also




<a href="https://msdn.microsoft.com/864bf814-43dd-4d2b-a5a7-fff12520accb">CMSPAddress</a>
 

 

