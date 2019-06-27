---
UID: NF:tom.ITextStory.GetProperty
title: ITextStory::GetProperty (tom.h)
author: windows-sdk-content
description: Gets the value of the specified property.
old-location: controls\itextstory_getproperty.htm
tech.root: Controls
ms.assetid: 1c24e9d8-c737-42f8-87d9-585b0054b6df
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetProperty, GetProperty method [Windows Controls], GetProperty method [Windows Controls],ITextStory interface, ITextStory interface [Windows Controls],GetProperty method, ITextStory.GetProperty, ITextStory::GetProperty, controls.itextstory_getproperty, tom/ITextStory::GetProperty
ms.topic: method
f1_keywords: 
 - "tom/ITextStory.GetProperty"
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
req.lib: 
req.dll: 
req.irql: 
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
req.typenames: 
req.redist: 
ms.custom: 19H1
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



Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/tom/nn-tom-itextstory">ITextStory</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextstory-setproperty">ITextStory::SetProperty</a>
 

 

