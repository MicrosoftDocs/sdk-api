---
UID: NF:tom.ITextFont2.GetProperty
title: ITextFont2::GetProperty method
author: windows-driver-content
description: Gets the value of the specified property.
old-location: controls\itextfont2_getproperty.htm
old-project: Controls
ms.assetid: 1894788a-5612-43a2-af77-131d02fe1261
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: GetProperty method [Windows Controls], GetProperty method [Windows Controls], ITextFont2 interface, GetProperty,ITextFont2.GetProperty, ITextFont2, ITextFont2 interface [Windows Controls], GetProperty method, ITextFont2::GetProperty, controls.itextfont2_getproperty, tom/ITextFont2::GetProperty
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
-	ITextFont2.GetProperty
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextFont2::GetProperty method


## -description


Gets the value of the specified property.


## -parameters




### -param Type [in]

Type: <b>long</b>

The property ID of the value to return.
See Remarks.


### -param pValue [out]

Type: <b>long*</b>

The property value.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



Property IDs are defined by the Text Object Model (TOM).  Here are how some of the TOM values are obtained:




## -see-also




<a href="https://msdn.microsoft.com/d2d43bfd-7cdf-458a-822d-e3965bfe2284">ITextFont2</a>



<a href="https://msdn.microsoft.com/c4d35fed-9bf5-431e-96c9-b1d51d51703a">ITextFont2::SetProperty</a>
 

 

