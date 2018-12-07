---
UID: NF:drt.DrtDeleteNullSecurityProvider
title: DrtDeleteNullSecurityProvider function
author: windows-sdk-content
description: DrtDeleteNullSecurityProvider function deletes a null security provider for a Distributed Routing Table.
old-location: p2p\drtdeletenullsecurityprovider.htm
tech.root: P2PSdk
ms.assetid: 950a43f3-1c1d-4fb3-988b-d58ac9eff2f8
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: DrtDeleteNullSecurityProvider, DrtDeleteNullSecurityProvider function [Distributed Routing Tables], drt/DrtDeleteNullSecurityProvider, p2p.drtdeletenullsecurityprovider
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: drt.h
req.include-header: 
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
req.lib: Drtprov.lib
req.dll: Drt.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - drt.dll
api_name:
 - DrtDeleteNullSecurityProvider
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DrtDeleteNullSecurityProvider function


## -description


The <b>DrtDeleteNullSecurityProvider</b> function deletes a null security provider for a Distributed Routing Table.


## -parameters




### -param pSecurityProvider [in]

Pointer to a <a href="https://msdn.microsoft.com/1eedfff3-d561-462e-bad0-45e7bc46fb1a">DRT_SECURITY_PROVIDER</a> structure specifying the security provider to delete.


## -returns



This function does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/1eedfff3-d561-462e-bad0-45e7bc46fb1a">DRT_SECURITY_PROVIDER</a>



<a href="https://msdn.microsoft.com/ba6e766f-784b-4609-8ad5-c1bfb0575f34">DrtCreateNullSecurityProvider</a>
 

 

