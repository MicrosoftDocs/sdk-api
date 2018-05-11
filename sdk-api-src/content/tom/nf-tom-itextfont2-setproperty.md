---
UID: NF:tom.ITextFont2.SetProperty
title: ITextFont2::SetProperty
author: windows-driver-content
description: Sets the value of the specified property.
old-location: controls\itextfont2_setproperty.htm
old-project: Controls
ms.assetid: c4d35fed-9bf5-431e-96c9-b1d51d51703a
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: ITextFont2 interface [Windows Controls],SetProperty method, ITextFont2.SetProperty, ITextFont2::SetProperty, SetProperty, SetProperty method [Windows Controls], SetProperty method [Windows Controls],ITextFont2 interface, controls.itextfont2_setproperty, tom/ITextFont2::SetProperty
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: tom.h
req.include-header: 
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
req.typenames: MANCODE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Msftedit.dll
api_name:
-	ITextFont2.SetProperty
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextFont2::SetProperty


## -description


Sets the value of the specified property.


## -parameters




### -param Type [in]

Type: <b>long</b>

The ID of the property value to set. Types are defined by TOM. For a list of types, see <a href="https://msdn.microsoft.com/1894788a-5612-43a2-af77-131d02fe1261">ITextFont2::GetProperty</a>.


### -param Value [in]

Type: <b>long</b>

The new property value.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/d2d43bfd-7cdf-458a-822d-e3965bfe2284">ITextFont2</a>



<a href="https://msdn.microsoft.com/1894788a-5612-43a2-af77-131d02fe1261">ITextFont2::GetProperty</a>
 

 

