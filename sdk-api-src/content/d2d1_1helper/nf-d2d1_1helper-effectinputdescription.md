---
UID: NF:d2d1_1helper.EffectInputDescription
title: EffectInputDescription function
author: windows-sdk-content
description: Creates a D2D1_EFFECT_INPUT_DESCRIPTION structure.
old-location: direct2d\effectinputdescription.htm
tech.root: Direct2D
ms.assetid: 3246476C-4110-43EC-88A3-55682A141383
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: EffectInputDescription, EffectInputDescription function [Direct2D], d2d1_1helper/EffectInputDescription, direct2d.effectinputdescription
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: d2d1_1helper.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - D2d1.dll
api_name:
 - EffectInputDescription
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# EffectInputDescription function


## -description


Creates a <a href="https://msdn.microsoft.com/2ce9405a-e36d-4b9e-b9d2-2a58b78696ac">D2D1_EFFECT_INPUT_DESCRIPTION</a> structure.


## -parameters




### -param effect

Type: <b><a href="https://msdn.microsoft.com/e90d1830-c356-48f1-ac7b-1d94c8c26569">ID2D1Effect</a>*</b>

The effect whose input connection is being specified.


### -param inputIndex

Type: <b>UINT32</b>

The input index of the effect that is being considered.


### -param inputRectangle

Type: <b><a href="https://msdn.microsoft.com/a961c0e3-fb76-4c07-b76e-47d8c09ada08">D2D1_RECT_F</a></b>

The amount of data that would be available on the input. This can be used to query this information when the data is not yet available. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/2ce9405a-e36d-4b9e-b9d2-2a58b78696ac">D2D1_EFFECT_INPUT_DESCRIPTION</a></b>

The filled description structure that describes the input to the effect.



