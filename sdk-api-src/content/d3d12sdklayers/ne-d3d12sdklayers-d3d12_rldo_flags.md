---
UID: NE:d3d12sdklayers.D3D12_RLDO_FLAGS
title: D3D12_RLDO_FLAGS
author: windows-sdk-content
description: Specifies options for the amount of information to report about a live device object's lifetime.
old-location: direct3d12\d3d12_rldo_flags.htm
tech.root: direct3d12
ms.assetid: FF868102-26FC-4541-9C21-0B8D6D4CF47B
ms.author: windowssdkdev
ms.date: 11/12/2018
ms.keywords: D3D12_RLDO_DETAIL, D3D12_RLDO_FLAGS, D3D12_RLDO_FLAGS enumeration, D3D12_RLDO_IGNORE_INTERNAL, D3D12_RLDO_NONE, D3D12_RLDO_SUMMARY, d3d12sdklayers/D3D12_RLDO_DETAIL, d3d12sdklayers/D3D12_RLDO_FLAGS, d3d12sdklayers/D3D12_RLDO_IGNORE_INTERNAL, d3d12sdklayers/D3D12_RLDO_NONE, d3d12sdklayers/D3D12_RLDO_SUMMARY, direct3d12.d3d12_rldo_flags
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
 - HeaderDef
api_location:
 - d3d12sdklayers.h
api_name:
 - D3D12_RLDO_FLAGS
product: Windows
targetos: Windows
req.typenames: D3D12_RLDO_FLAGS
req.redist: 
---

# D3D12_RLDO_FLAGS enumeration


## -description


Specifies options for the amount of information to report about a live device object's lifetime.


        


## -enum-fields




### -field D3D12_RLDO_NONE


### -field D3D12_RLDO_SUMMARY

Obtain a summary about a live device object's lifetime. 




### -field D3D12_RLDO_DETAIL

Obtain detailed information about a live device object's lifetime. 


          


### -field D3D12_RLDO_IGNORE_INTERNAL

Internal use only.


## -remarks



This enumeration is used by <a href="https://msdn.microsoft.com/37771598-DC2E-42FA-B17D-A187164A3314">ID3D12DebugDevice::ReportLiveDeviceObjects</a>. 




## -see-also




<a href="https://msdn.microsoft.com/6E76C857-128E-4F0E-9711-72C4CF6C835C">Debug Layer Enumerations</a>
 

 

