---
UID: NF:tom.ITextRow.GetProperty
title: ITextRow::GetProperty method
author: windows-driver-content
description: Gets the value of the specified property.
old-location: controls\itextrow_getproperty.htm
old-project: Controls
ms.assetid: ed47033f-14b2-4ca1-89be-f2eab3d148ef
ms.author: windowsdriverdev
ms.date: 3/31/2018
ms.keywords: GetProperty method [Windows Controls], GetProperty method [Windows Controls], ITextRow interface, GetProperty,ITextRow.GetProperty, ITextRow, ITextRow interface [Windows Controls], GetProperty method, ITextRow::GetProperty, controls.itextrow_getproperty, tom/ITextRow::GetProperty
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
-	ITextRow.GetProperty
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextRow::GetProperty method


## -description


Gets the value of the specified property. 


## -parameters




### -param Type [in]

Type: <b>long</b>

The ID of the property to retrieve.


### -param pValue [out]

Type: <b>long*</b>

The value for the property.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



Currently, no extra properties are defined.




## -see-also




<a href="https://msdn.microsoft.com/49f5ffc1-d615-4d07-9f41-1c5f0dd9045b">ITextRow</a>



<a href="https://msdn.microsoft.com/d43172b9-c717-41b2-ba22-aa164a595140">ITextRow::SetProperty</a>
 

 

