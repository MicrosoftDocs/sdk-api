---
UID: NF:wbemdisp.ISWbemRefresher.get_AutoReconnect
title: ISWbemRefresher::get_AutoReconnect
author: windows-sdk-content
description: The AutoReconnect property of the SWbemRefresher object is a Boolean value that indicates whether the refresher automatically reconnects to a remote provider if the connection is broken.
old-location: wmi\swbemrefresher_autoreconnect.htm
old-project: WmiSdk
ms.assetid: 3be24128-8a35-44b0-befd-8b8937eff1b7
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: AutoReconnect property [Windows Management Instrumentation], AutoReconnect property [Windows Management Instrumentation],ISWbemRefresher interface, AutoReconnect property [Windows Management Instrumentation],SWbemRefresher object, ISWbemRefresher interface [Windows Management Instrumentation],AutoReconnect property, ISWbemRefresher.get_AutoReconnect, ISWbemRefresher::get_AutoReconnect, SWbemRefresher object [Windows Management Instrumentation],AutoReconnect property, SWbemRefresher.AutoReconnect, _hmm_swbemrefresher.autoreconnect, get_AutoReconnect, wmi.swbemrefresher_autoreconnect
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wbemdisp.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: Wbemdisp.tlb
tech.root: 
req.typenames: WbemTimeout
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wbemdisp.dll
api_name:
 - SWbemRefresher.AutoReconnect
 - ISWbemRefresher.AutoReconnect
 - ISWbemRefresher.get_AutoReconnect
product: Windows
targetos: Windows
req.lib: 
req.dll: Wbemdisp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISWbemRefresher::get_AutoReconnect


## -description



The 
<b>AutoReconnect</b> property of the 
<a href="https://msdn.microsoft.com/cc5872a1-932b-4b68-9f5e-a91d35c8e117">SWbemRefresher</a> object is a Boolean value that indicates whether the refresher automatically reconnects to a remote provider if the connection is broken.



For an explanation of this syntax, see 
<a href="https://msdn.microsoft.com/889e6322-96f6-4a24-a084-e3b7bfa94a40">Document Conventions for the Scripting API</a>.

This property is read-only.


## -parameters


## -remarks



Modifying this property affects only objects in the refresher that are backed by a high-performance provider. If the provider is not a high-performance provider, then setting the 
<b>AutoReconnect</b> property to <b>TRUE</b> has no effect because the 
<a href="https://msdn.microsoft.com/cc5872a1-932b-4b68-9f5e-a91d35c8e117">SWbemRefresher</a> object  never reconnects.




## -see-also




<a href="https://msdn.microsoft.com/cc5872a1-932b-4b68-9f5e-a91d35c8e117">SWbemRefresher</a>
 

 

