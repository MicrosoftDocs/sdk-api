---
UID: NF:propsys.IPropertyDescription2.GetImageReferenceForValue
title: IPropertyDescription2::GetImageReferenceForValue
author: windows-sdk-content
description: Gets the image reference associated with a property value.
old-location: properties\IPropertyDescription2_GetImageReferenceForValue.htm
old-project: properties
ms.assetid: d5831e8c-0b98-4cdc-946e-3c359a04caed
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetImageReferenceForValue, GetImageReferenceForValue method [Windows Properties], GetImageReferenceForValue method [Windows Properties],IPropertyDescription2 interface, IPropertyDescription2 interface [Windows Properties],GetImageReferenceForValue method, IPropertyDescription2.GetImageReferenceForValue, IPropertyDescription2::GetImageReferenceForValue, properties.IPropertyDescription2_GetImageReferenceForValue, propsys/IPropertyDescription2::GetImageReferenceForValue, shell.IPropertyDescription2_GetImageReferenceForValue, shell_IPropertyDescription2_GetImageReferenceForValue
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: propsys.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Propsys.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: PSC_STATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Propsys.h
api_name:
 - IPropertyDescription2.GetImageReferenceForValue
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IPropertyDescription2::GetImageReferenceForValue


## -description


Gets the image reference associated with a property value.


## -parameters




### -param propvar [in]

Type: <b>REFPROPVARIANT</b>

The <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> for which to get an image.


### -param ppszImageRes [out]

Type: <b>LPWSTR*</b>

A pointer to a buffer that receives, when this method returns successfully, a string of the form &lt;dll name&gt;,-&lt;resid&gt; that is suitable to be passed to <a href="https://msdn.microsoft.com/1ded2f0f-0e11-4730-ab7b-16536e7f4435">PathParseIconLocation</a>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



