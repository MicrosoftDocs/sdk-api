---
UID: NF:propsys.IPropertyEnumType2.GetImageReference
title: IPropertyEnumType2::GetImageReference (propsys.h)
description: Retrieves the image reference associated with a property enumeration.
helpviewer_keywords: ["GetImageReference","GetImageReference method [Windows Properties]","GetImageReference method [Windows Properties]","IPropertyEnumType2 interface","IPropertyEnumType2 interface [Windows Properties]","GetImageReference method","IPropertyEnumType2.GetImageReference","IPropertyEnumType2::GetImageReference","_shell_IPropertyEnumType2_GetImageReference","properties.IPropertyEnumType2_GetImageReference","propsys/IPropertyEnumType2::GetImageReference","shell.IPropertyEnumType2_GetImageReference"]
old-location: properties\IPropertyEnumType2_GetImageReference.htm
tech.root: properties
ms.assetid: 3b519cb1-cfea-4242-99f4-af290d622c38
ms.date: 12/05/2018
ms.keywords: GetImageReference, GetImageReference method [Windows Properties], GetImageReference method [Windows Properties],IPropertyEnumType2 interface, IPropertyEnumType2 interface [Windows Properties],GetImageReference method, IPropertyEnumType2.GetImageReference, IPropertyEnumType2::GetImageReference, _shell_IPropertyEnumType2_GetImageReference, properties.IPropertyEnumType2_GetImageReference, propsys/IPropertyEnumType2::GetImageReference, shell.IPropertyEnumType2_GetImageReference
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPropertyEnumType2::GetImageReference
 - propsys/IPropertyEnumType2::GetImageReference
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Propsys.h
api_name:
 - IPropertyEnumType2.GetImageReference
---

# IPropertyEnumType2::GetImageReference


## -description

Retrieves the image reference associated with a property enumeration.

## -parameters

### -param ppszImageRes [out]

Type: <b>LPWSTR*</b>

A pointer to a buffer that, when this method returns successfully, receives a string of the form &lt;dll name&gt;,-&lt;resid&gt; that is suitable to be passed to <a href="/windows/desktop/api/shlwapi/nf-shlwapi-pathparseiconlocationa">PathParseIconLocation</a>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.