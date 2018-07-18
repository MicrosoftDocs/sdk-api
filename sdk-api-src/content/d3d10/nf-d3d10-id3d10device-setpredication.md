---
UID: NF:d3d10.ID3D10Device.SetPredication
title: ID3D10Device::SetPredication
author: windows-sdk-content
description: Set a rendering predicate.
old-location: direct3d10\id3d10device_setpredication.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_setpredication.htm
ms.author: windowssdkdev
ms.date: 06/29/2018
ms.keywords: 20a67636-3d02-6716-b38e-39b2f601230b, ID3D10Device interface [Direct3D 10],SetPredication method, ID3D10Device.SetPredication, ID3D10Device::SetPredication, SetPredication, SetPredication method [Direct3D 10], SetPredication method [Direct3D 10],ID3D10Device interface, d3d10/ID3D10Device::SetPredication, direct3d10.id3d10device_setpredication
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d10.h
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
req.typenames: D3D10_USAGE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10.lib
 - D3D10.dll
api_name:
 - ID3D10Device.SetPredication
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: 
req.irql: 
---

# ID3D10Device::SetPredication


## -description


Set a rendering predicate.


## -parameters




### -param pPredicate [in]

Type: <b><a href="https://msdn.microsoft.com/library/Bb173822(v=VS.85).aspx">ID3D10Predicate</a>*</b>

Pointer to a predicate (see <a href="https://msdn.microsoft.com/library/Bb173822(v=VS.85).aspx">ID3D10Predicate</a>). A <b>NULL</b> value indicates "no" predication; in this case, the value of PredicateValue is irrelevent but will be preserved for <a href="https://msdn.microsoft.com/library/Bb173573(v=VS.85).aspx">ID3D10Device::GetPredication</a>.


### -param PredicateValue [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

If <b>TRUE</b>, rendering will be affected by when the predicate's conditions are met. If <b>FALSE</b>, rendering will be affected when the conditions are not met.


## -returns



Returns nothing.




## -remarks



The predicate must be in the "issued" or "signaled" state to be used for predication. While the predicate is set for predication, calls to <a href="https://msdn.microsoft.com/library/Bb173501(v=VS.85).aspx">ID3D10Asynchronous::Begin</a> and <a href="https://msdn.microsoft.com/library/Bb173502(v=VS.85).aspx">ID3D10Asynchronous::End</a> are invalid.

This method is used to denote that subsequent rendering and resource manipulation commands are not actually performed if the resulting Predicate data of the Predicate is equal to the PredicateValue. However, some Predicates are only hints, so they may not actually prevent operations from being performed. 

The primary usefulness of Predication is to allow an application to issue graphics commands without taking the performance hit of spinning, waiting for <a href="https://msdn.microsoft.com/library/Bb173503(v=VS.85).aspx">ID3D10Asynchronous::GetData</a> to return. So, Predication can occur while <b>ID3D10Asynchronous::GetData</b> returns S_FALSE. Another way to think of it: an application can also use Predication as a fallback, if it is possible that <b>ID3D10Asynchronous::GetData</b> returns S_FALSE. If <b>ID3D10Asynchronous::GetData</b> returns S_OK, the application can skip calling the graphics commands manually with it's own application logic.




## -see-also




<a href="https://msdn.microsoft.com/library/Bb173528(v=VS.85).aspx">ID3D10Device Interface</a>
 

 

