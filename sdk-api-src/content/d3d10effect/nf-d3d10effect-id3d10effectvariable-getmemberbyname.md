---
UID: NF:d3d10effect.ID3D10EffectVariable.GetMemberByName
title: ID3D10EffectVariable::GetMemberByName
author: windows-sdk-content
description: Get a structure member by name.
old-location: direct3d10\id3d10effectvariable_getmemberbyname.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectvariable_getmemberbyname.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetMemberByName, GetMemberByName method [Direct3D 10], GetMemberByName method [Direct3D 10],ID3D10EffectVariable interface, ID3D10EffectVariable interface [Direct3D 10],GetMemberByName method, ID3D10EffectVariable.GetMemberByName, ID3D10EffectVariable::GetMemberByName, bca41608-f225-d8f7-81c8-fb65153d754a, d3d10effect/ID3D10EffectVariable::GetMemberByName, direct3d10.id3d10effectvariable_getmemberbyname
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d10effect.h
req.include-header: 
req.redist: 
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
req.typenames: D3D10_DEVICE_STATE_TYPES
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10Effect.h
api_name:
 - ID3D10EffectVariable.GetMemberByName
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D10EffectVariable::GetMemberByName


## -description


Get a structure member by name.


## -parameters




### -param Name [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCSTR</a></b>

Member name.


## -returns



Type: <b><a href="https://msdn.microsoft.com/55bfed47-6f5a-4eed-8389-b291e00c6f69">ID3D10EffectVariable</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/55bfed47-6f5a-4eed-8389-b291e00c6f69">ID3D10EffectVariable Interface</a>.




## -remarks



If the effect variable is an structure, use this method to look up a member by name.




## -see-also




<a href="https://msdn.microsoft.com/55bfed47-6f5a-4eed-8389-b291e00c6f69">ID3D10EffectVariable Interface</a>
 

 

