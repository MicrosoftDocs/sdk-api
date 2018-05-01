---
UID: NF:propsys.IPropertyEnumType2.GetImageReference
title: IPropertyEnumType2::GetImageReference method
author: windows-driver-content
description: Retrieves the image reference associated with a property enumeration.
old-location: properties\IPropertyEnumType2_GetImageReference.htm
old-project: properties
ms.assetid: 3b519cb1-cfea-4242-99f4-af290d622c38
ms.author: windowsdriverdev
ms.date: 4/5/2018
ms.keywords: GetImageReference method [Windows Properties], GetImageReference method [Windows Properties], IPropertyEnumType2 interface, GetImageReference,IPropertyEnumType2.GetImageReference, IPropertyEnumType2, IPropertyEnumType2 interface [Windows Properties], GetImageReference method, IPropertyEnumType2::GetImageReference, _shell_IPropertyEnumType2_GetImageReference, properties.IPropertyEnumType2_GetImageReference, propsys/IPropertyEnumType2::GetImageReference, shell.IPropertyEnumType2_GetImageReference
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: PSC_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Propsys.h
api_name:
-	IPropertyEnumType2.GetImageReference
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IPropertyEnumType2::GetImageReference method


## -description


Retrieves the image reference associated with a property enumeration.


## -parameters




### -param ppszImageRes [out]

Type: <b>LPWSTR*</b>

A pointer to a buffer that, when this method returns successfully, receives a string of the form &lt;dll name&gt;,-&lt;resid&gt; that is suitable to be passed to <a href="https://msdn.microsoft.com/1ded2f0f-0e11-4730-ab7b-16536e7f4435">PathParseIconLocation</a>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



