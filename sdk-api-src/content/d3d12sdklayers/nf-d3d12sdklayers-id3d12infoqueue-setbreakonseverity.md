---
UID: NF:d3d12sdklayers.ID3D12InfoQueue.SetBreakOnSeverity
title: ID3D12InfoQueue::SetBreakOnSeverity
author: windows-sdk-content
description: Set a message severity level to break on when a message with that severity level passes through the storage filter.
old-location: direct3d12\id3d12infoqueue_setbreakonseverity.htm
tech.root: direct3d12
ms.assetid: 5A055726-B17A-4058-A964-F50BE2FB1FFA
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: ID3D12InfoQueue interface,SetBreakOnSeverity method, ID3D12InfoQueue.SetBreakOnSeverity, ID3D12InfoQueue::SetBreakOnSeverity, SetBreakOnSeverity, SetBreakOnSeverity method, SetBreakOnSeverity method,ID3D12InfoQueue interface, d3d12sdklayers/ID3D12InfoQueue::SetBreakOnSeverity, direct3d12.id3d12infoqueue_setbreakonseverity
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d12sdklayers.h
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
 - d3d12sdklayers.h
api_name:
 - ID3D12InfoQueue.SetBreakOnSeverity
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D12InfoQueue::SetBreakOnSeverity


## -description


Set a message severity level to break on when a message with that severity level passes through the storage filter.




## -parameters




### -param Severity [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dn950147(v=VS.85).aspx">D3D12_MESSAGE_SEVERITY</a></b>

A message severity level to break on.

          


### -param bEnable [in]

Type: <b>BOOL</b>

Turns this breaking condition on or off (true for on, false for off).




## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

This method returns one of the <a href="https://msdn.microsoft.com/en-us/library/Dn706075(v=VS.85).aspx">Direct3D 12 Return Codes</a>. 
          




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dn950163(v=VS.85).aspx">ID3D12InfoQueue</a>
 

 

