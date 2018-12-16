---
UID: NF:drt.DrtGetSearchPath
title: DrtGetSearchPath function
author: windows-sdk-content
description: DrtGetSearchPath function returns a list of nodes contacted during the search operation.
old-location: p2p\drtgetsearchpath.htm
tech.root: P2PSdk
ms.assetid: d095acbe-30bf-4449-bd00-a9f8813111c5
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DrtGetSearchPath, DrtGetSearchPath function [Peer Networking], drt/DrtGetSearchPath, p2p.drtgetsearchpath
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
req.lib: Drt.lib
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
 - DrtGetSearchPath
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DrtGetSearchPath function


## -description


The <b>DrtGetSearchPath</b> function returns a list of nodes contacted during the search operation.


## -parameters




### -param hSearchContext [in]

Handle to the search context. This parameter is returned by the <a href="https://msdn.microsoft.com/d43634d5-eb0a-4f84-9248-977c544db984">DrtStartSearch</a> function.


### -param ulSearchPathSize [in, out]

The size of the search path which represents the number of nodes utilized in the search operation.


### -param pSearchPath [out]

Pointer to a <a href="https://msdn.microsoft.com/a795dff7-4182-42ad-b14b-142a6c1312c7">DRT_ADDRESS_LIST</a> structure containing the list of addresses.


## -returns



This function returns S_OK on success.




## -see-also




<a href="https://msdn.microsoft.com/a795dff7-4182-42ad-b14b-142a6c1312c7">DRT_ADDRESS_LIST</a>



<a href="https://msdn.microsoft.com/dadd5f2a-2584-4046-8cdf-4d6ea97cc878">DrtGetSearchPathSize</a>
 

 

