---
UID: NF:drt.DrtGetSearchPathSize
title: DrtGetSearchPathSize function (drt.h)
author: windows-sdk-content
description: DrtGetSearchPathSize function returns the size of the search path, which represents the number of nodes utilized in the search operation.
old-location: p2p\drtgetsearchpathsize.htm
tech.root: P2PSdk
ms.assetid: dadd5f2a-2584-4046-8cdf-4d6ea97cc878
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DrtGetSearchPathSize, DrtGetSearchPathSize function [Peer Networking], drt/DrtGetSearchPathSize, p2p.drtgetsearchpathsize
ms.topic: function
f1_keywords:
- drt/DrtGetSearchPathSize
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
- DrtGetSearchPathSize
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DrtGetSearchPathSize function


## -description


The <b>DrtGetSearchPathSize</b> function returns the size of the search path, which represents the number of nodes utilized in the search operation.


## -parameters




### -param hSearchContext [in]

Handle to the search context. This parameter is returned by the <a href="https://docs.microsoft.com/windows/desktop/api/drt/nf-drt-drtstartsearch">DrtStartSearch</a> function.


### -param pulSearchPathSize [out]

Pointer to a <b>ULONG</b> value that indicates the size of the search path. 


## -returns



This function returns S_OK on success.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/drt/ns-drt-drt_address_list">DRT_ADDRESS_LIST</a>



<a href="https://docs.microsoft.com/windows/desktop/api/drt/nf-drt-drtgetsearchpathsize">DrtGetSearchPathSize</a>
 

 

