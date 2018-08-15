---
UID: NF:tom.ITextPara2.SetEffects
title: ITextPara2::SetEffects
author: windows-sdk-content
description: Sets the paragraph format effects.
old-location: controls\itextpara2_seteffects.htm
old-project: controls
ms.assetid: e7184de4-b416-4f28-8f10-c89ffcccf1a1
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ITextPara2 interface [Windows Controls],SetEffects method, ITextPara2.SetEffects, ITextPara2::SetEffects, SetEffects, SetEffects method [Windows Controls], SetEffects method [Windows Controls],ITextPara2 interface, controls.itextpara2_seteffects, tom/ITextPara2::SetEffects
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: tom.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: MANCODE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msftedit.dll
api_name:
 - ITextPara2.SetEffects
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextPara2::SetEffects


## -description


Sets the paragraph format effects.


## -parameters




### -param Value [in]

Type: <b>long</b>

The paragraph effects value.

This value can be a combination of the flags defined in the table for <a href="https://msdn.microsoft.com/7f672cc9-e8f3-416a-8f41-9b71ca1858a1">ITextPara2::GetEffects</a>.


### -param Mask [in]

Type: <b>long</b>

The desired mask.

This value can be a combination of the flags defined in the table for <a href="https://msdn.microsoft.com/7f672cc9-e8f3-416a-8f41-9b71ca1858a1">ITextPara2::GetEffects</a>. 

Only effects with the corresponding mask flag set are modified.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/31a0849f-c651-4178-b1ff-a4333bcde5d9">ITextPara2</a>



<a href="https://msdn.microsoft.com/7f672cc9-e8f3-416a-8f41-9b71ca1858a1">ITextPara2::GetEffects</a>
 

 

