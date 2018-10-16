---
UID: NF:dcomp.IDCompositionDevice2.CreateEffectGroup
title: IDCompositionDevice2::CreateEffectGroup
author: windows-sdk-content
description: Creates an object that represents multiple effects to be applied to a visual subtree.
old-location: directcomp\idcompositiondevice2_createeffectgroup.htm
tech.root: directcomp
ms.assetid: 07AF43F9-1050-48C5-B37B-787B5CC60E9D
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: CreateEffectGroup, CreateEffectGroup method [DirectComposition], CreateEffectGroup method [DirectComposition],IDCompositionDevice2 interface, IDCompositionDevice2 interface [DirectComposition],CreateEffectGroup method, IDCompositionDevice2.CreateEffectGroup, IDCompositionDevice2::CreateEffectGroup, dcomp/IDCompositionDevice2::CreateEffectGroup, directcomp.idcompositiondevice2_createeffectgroup
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dcomp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dcomp.lib
req.dll: Dcomp.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dcomp.dll
api_name:
 - IDCompositionDevice2.CreateEffectGroup
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDCompositionDevice2::CreateEffectGroup


## -description


Creates an object that represents multiple effects to be applied to a visual subtree.


## -parameters




### -param effectGroup [out]

Type: <b><a href="https://msdn.microsoft.com/B8C5A4D8-F161-4383-B117-B89E85C65B19">IDCompositionEffectGroup</a>**</b>

The new effect group object. This parameter must not be NULL.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/8DFBFC34-DBD0-4731-8305-B33E90C96C54">DirectComposition Error Codes</a>  for a list of error codes.




## -remarks



An effect group enables an application to apply multiple effects to a single visual subtree. 

A new effect group has a default opacity value of 1.0 and no 3D transformations.

To set the opacity and transform values, use the corresponding methods on the <a href="https://msdn.microsoft.com/B8C5A4D8-F161-4383-B117-B89E85C65B19">IDCompositionEffectGroup</a> that was created.




## -see-also




<a href="https://msdn.microsoft.com/0E5D0AEC-63A3-4A44-9A0B-D1E26789CAB0">IDCompositionDevice2</a>



<a href="https://msdn.microsoft.com/CCA785F6-869C-460A-AF54-573BDE798685">IDCompositionVisual::SetEffect</a>
 

 

