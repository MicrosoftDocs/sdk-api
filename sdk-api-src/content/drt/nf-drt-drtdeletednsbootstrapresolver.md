---
UID: NF:drt.DrtDeleteDnsBootstrapResolver
title: DrtDeleteDnsBootstrapResolver function
author: windows-sdk-content
description: DrtDeleteDnsBootstrapResolver function deletes a DNS Bootstrap Provider instance.
old-location: p2p\drtdeletednsbootstrapresolver.htm
old-project: p2psdk
ms.assetid: fc3d0b6a-1bf3-41f9-82b6-965c285bc6c7
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: DrtDeleteDnsBootstrapResolver, DrtDeleteDnsBootstrapResolver function [Distributed Routing Tables], drt/DrtDeleteDnsBootstrapResolver, p2p.drtdeletednsbootstrapresolver
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: drt.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 Professional [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: DRT_REGISTRATION_STATE, *PDRT_REGISTRATION_STATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - drt.dll
api_name:
 - DrtDeleteDnsBootstrapResolver
product: Windows
targetos: Windows
req.lib: Drtprov.lib
req.dll: Drt.dll
req.irql: 
---

# DrtDeleteDnsBootstrapResolver function


## -description


The <b>DrtDeleteDnsBootstrapResolver</b> function deletes a DNS Bootstrap Provider instance.


## -parameters




### -param pResolver [in]

Pointer to a DRT_BOOTSTRAP_PROVIDER instance specifying the security provider to delte.


## -returns



This function does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/f64edf7f-379f-41e2-9a86-ba9aeee0f2d7">DRT_BOOTSTRAP_PROVIDER</a>



<a href="https://msdn.microsoft.com/d4a92dd3-d66a-4c27-9180-f9c148735a4a">DrtCreateDnsBootstrapResolver</a>
 

 

