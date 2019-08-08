---
UID: NF:drt.DrtGetSearchPath
title: DrtGetSearchPath function (drt.h)
author: windows-sdk-content
description: DrtGetSearchPath function returns a list of nodes contacted during the search operation.
old-location: p2p\drtgetsearchpath.htm
tech.root: P2PSdk
ms.assetid: d095acbe-30bf-4449-bd00-a9f8813111c5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DrtGetSearchPath, DrtGetSearchPath function [Peer Networking], drt/DrtGetSearchPath, p2p.drtgetsearchpath
ms.topic: function
f1_keywords:
- drt/DrtGetSearchPath
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
ms.custom: 19H1
---

# DrtGetSearchPath function


## -description


The <b>DrtGetSearchPath</b> function returns a list of nodes contacted during the search operation.


## -parameters




### -param hSearchContext [in]

Handle to the search context. This parameter is returned by the <a href="https://docs.microsoft.com/windows/desktop/api/drt/nf-drt-drtstartsearch">DrtStartSearch</a> function.


### -param ulSearchPathSize [in, out]

The size of the search path which represents the number of nodes utilized in the search operation.


### -param pSearchPath [out]

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/drt/ns-drt-drt_address_list">DRT_ADDRESS_LIST</a> structure containing the list of addresses.


## -returns



This function returns S_OK on success.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/drt/ns-drt-drt_address_list">DRT_ADDRESS_LIST</a>



<a href="https://docs.microsoft.com/windows/desktop/api/drt/nf-drt-drtgetsearchpathsize">DrtGetSearchPathSize</a>
 

 

