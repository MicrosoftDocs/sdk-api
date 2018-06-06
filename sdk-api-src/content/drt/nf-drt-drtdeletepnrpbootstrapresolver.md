---
UID: NF:drt.DrtDeletePnrpBootstrapResolver
title: DrtDeletePnrpBootstrapResolver function
author: windows-sdk-content
description: DrtDeletePnrpBootstrapResolver function deletes a bootstrap resolver based on the Peer Name Resolution Protocol (PNRP).
old-location: p2p\drtdeletepnrpbootstrapresolver.htm
old-project: P2PSdk
ms.assetid: 0ff7bcc6-548b-475a-8a83-1ca50dbe333d
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: DrtDeletePnrpBootstrapResolver, DrtDeletePnrpBootstrapResolver function [Peer Networking], drt/DrtDeletePnrpBootstrapResolver, p2p.drtdeletepnrpbootstrapresolver
ms.prod: windows
ms.technology: windows-sdk
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
 - DrtDeletePnrpBootstrapResolver
product: Windows
targetos: Windows
req.lib: Drtprov.lib
req.dll: Drt.dll
req.irql: 
---

# DrtDeletePnrpBootstrapResolver function


## -description


The <b>DrtDeletePnrpBootstrapResolver</b> function deletes a  bootstrap resolver based on the <a href="https://msdn.microsoft.com/6bf2cb09-c03a-4f6b-ba6c-670cf7219cc8">Peer Name Resolution Protocol</a> (PNRP).


## -parameters




### -param pResolver [in]

Pointer to the created PNRP bootstrap resolver to be deleted.


## -returns



This function does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/5bd64f10-abb8-4cba-8ebd-780a6a0c7074">DrtCreatePnrpBootstrapResolver</a>
 

 

