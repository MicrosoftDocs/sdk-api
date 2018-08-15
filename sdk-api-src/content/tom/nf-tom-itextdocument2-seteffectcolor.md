---
UID: NF:tom.ITextDocument2.SetEffectColor
title: ITextDocument2::SetEffectColor
author: windows-sdk-content
description: Specifies the color to use for special text attributes.
old-location: controls\itextdocument2_seteffectcolor.htm
old-project: controls
ms.assetid: 6371b525-96da-42a7-8cee-228b47208f46
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ITextDocument2 interface [Windows Controls],SetEffectColor method, ITextDocument2.SetEffectColor, ITextDocument2::SetEffectColor, SetEffectColor, SetEffectColor method [Windows Controls], SetEffectColor method [Windows Controls],ITextDocument2 interface, controls.itextdocument2_seteffectcolor, tom/ITextDocument2::SetEffectColor
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
 - ITextDocument2.SetEffectColor
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextDocument2::SetEffectColor


## -description


Specifies the color to use for special text attributes.


## -parameters




### -param Index [in]

Type: <b>long</b>

The index of the color to retrieve. For a list of values, see <a href="https://msdn.microsoft.com/4bc2740e-852f-430b-913e-5d28baec3272">GetEffectColor</a>.


### -param Value [in]

Type: <b>long</b>

The new color for the specified index.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



The first 16 index values are for special underline colors. If an index between 1 and 16 hasn't been defined by a call to the <b>ITextDocument2:SetEffectColor</b> method, the corresponding Microsoft Word default color is used. 




## -see-also




<a href="https://msdn.microsoft.com/0b0a54d7-7606-41f6-b8be-6367d9180ef4">ITextDocument2</a>



<a href="https://msdn.microsoft.com/4bc2740e-852f-430b-913e-5d28baec3272">ITextDocument2::GetEffectColor</a>
 

 

