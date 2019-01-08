---
UID: NF:wtsprotocol.IWRdsWddmIddProps.OnDriverUnload
title: IWRdsWddmIddProps::OnDriverUnload
author: windows-sdk-content
description: Termsrv uses this method to tell the protocol stack that PnP unloaded the WDDM ID driver.
old-location: termserv\iwrdswddmiddprops_ondriverunload.htm
tech.root: termserv
ms.assetid: D61C38FD-0298-4363-8A09-D0C2844C23CA
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWRdsWddmIddProps interface [Remote Desktop Services],OnDriverUnload method, IWRdsWddmIddProps.OnDriverUnload, IWRdsWddmIddProps::OnDriverUnload, OnDriverUnload, OnDriverUnload method [Remote Desktop Services], OnDriverUnload method [Remote Desktop Services],IWRdsWddmIddProps interface, termserv.iwrdswddmiddprops_ondriverunload, wtsprotocol/IWRdsWddmIddProps::OnDriverUnload
ms.topic: method
req.header: wtsprotocol.h
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
 - Wtsprotocol.h
api_name:
 - IWRdsWddmIddProps.OnDriverUnload
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWRdsWddmIddProps::OnDriverUnload


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

Termsrv uses this method to tell the protocol stack that PnP unloaded the
    WDDM ID driver.


## -parameters




### -param SessionId [in]

ID of a session driver is unloaded from.


## -returns



Returns S_OK or error code




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Mt832805(v=VS.85).aspx">IWRdsWddmIddProps</a>
 

 

