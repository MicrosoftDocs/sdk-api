---
UID: NF:tom.ITextFont2.GetPropertyInfo
title: ITextFont2::GetPropertyInfo
author: windows-driver-content
description: Gets the property type and value of the specified extra propety.
old-location: controls\itextfont2_getpropertyinfo.htm
old-project: Controls
ms.assetid: bea8f6da-f781-430f-b1cd-c28e11cc61bb
ms.author: windowsdriverdev
ms.date: 4/27/2018
ms.keywords: GetPropertyInfo, GetPropertyInfo method [Windows Controls], GetPropertyInfo method [Windows Controls],ITextFont2 interface, ITextFont2 interface [Windows Controls],GetPropertyInfo method, ITextFont2.GetPropertyInfo, ITextFont2::GetPropertyInfo, controls.itextfont2_getpropertyinfo, tom/ITextFont2::GetPropertyInfo
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
-	ITextFont2.GetPropertyInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextFont2::GetPropertyInfo


## -description


Gets the property type and value of the specified extra propety.


## -parameters




### -param Index [in]

Type: <b>long</b>

The collection index of the extra property.


### -param pType [out]

Type: <b>long*</b>

The property ID.


### -param pValue [out]

Type: <b>long*</b>

The property value.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/d2d43bfd-7cdf-458a-822d-e3965bfe2284">ITextFont2</a>
 

 

