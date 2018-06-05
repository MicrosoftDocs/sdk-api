---
UID: NF:d3d11_4.ID3D11Multithread.Leave
title: ID3D11Multithread::Leave
author: windows-sdk-content
description: Leave a device's critical section.
old-location: direct3d11\id3d11multithread_leave.htm
old-project: direct3d11
ms.assetid: CECBE440-3F9E-4649-B257-BAD3E7F5CF2F
ms.author: windowssdkdev
ms.date: 04/06/2018
ms.keywords: ID3D11Multithread interface [Direct3D 11],Leave method, ID3D11Multithread.Leave, ID3D11Multithread::Leave, Leave, Leave method [Direct3D 11], Leave method [Direct3D 11],ID3D11Multithread interface, d3d11_4/ID3D11Multithread::Leave, direct3d11.id3d11multithread_leave
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d11_4.h
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
tech.root: 
req.typenames: D3D11_UNORDERED_ACCESS_VIEW_DESC1
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	d3d11_4.dll
api_name:
-	ID3D11Multithread.Leave
product: Windows
targetos: Windows
req.lib: D3d11_4.lib
req.dll: D3d11_4.dll
req.irql: 
---

# ID3D11Multithread::Leave


## -description


Leave a device's critical section.


## -parameters






## -returns



This method does not return a value.




## -remarks



This function is typically used in multithreaded applications when there is a series of graphics commands 
		  that must happen in order. <a href="https://msdn.microsoft.com/A742D03A-0A47-4B08-952A-836A272D1519">Enter</a> is typically called at the beginning of a series of graphics commands, and this function is typically 
		  called after those graphics commands.




## -see-also




<a href="https://msdn.microsoft.com/1A07694E-7D61-4A59-82E3-048F04C8D57A">ID3D11Multithread</a>
 

 

