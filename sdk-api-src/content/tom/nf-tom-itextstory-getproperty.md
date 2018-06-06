---
UID: NF:tom.ITextStory.GetProperty
title: ITextStory::GetProperty
author: windows-sdk-content
description: Gets the value of the specified property.
old-location: controls\itextstory_getproperty.htm
old-project: Controls
ms.assetid: 1c24e9d8-c737-42f8-87d9-585b0054b6df
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: GetProperty, GetProperty method [Windows Controls], GetProperty method [Windows Controls],ITextStory interface, ITextStory interface [Windows Controls],GetProperty method, ITextStory.GetProperty, ITextStory::GetProperty, controls.itextstory_getproperty, tom/ITextStory::GetProperty
ms.prod: windows
ms.technology: windows-sdk
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
req.idl: Tom.idl
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
 - tom.h
api_name:
 - ITextStory.GetProperty
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextStory::GetProperty


## -description


Gets the value of the specified property.


## -parameters




### -param Type [in]

Type: <b>long</b>

The ID of the property.  Currently, no extra properties are defined.


### -param pValue [out]

Type: <b>long*</b>

The property value.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/8b52c6e8-c250-4cfb-979e-770df9f94010">ITextStory</a>



<a href="https://msdn.microsoft.com/432afe58-a1ed-45aa-b018-bf608bbb7e2a">ITextStory::SetProperty</a>
 

 

