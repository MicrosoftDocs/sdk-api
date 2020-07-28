---
UID: NF:dwrite.IDWriteFactory.CreateNumberSubstitution
title: IDWriteFactory::CreateNumberSubstitution (dwrite.h)
description: Creates a number substitution object using a locale name, substitution method, and an indicator whether to ignore user overrides (use NLS defaults for the given culture instead).
helpviewer_keywords: ["CreateNumberSubstitution","CreateNumberSubstitution method [Direct Write]","CreateNumberSubstitution method [Direct Write]","IDWriteFactory interface","IDWriteFactory interface [Direct Write]","CreateNumberSubstitution method","IDWriteFactory.CreateNumberSubstitution","IDWriteFactory::CreateNumberSubstitution","directwrite.IDWriteFactory_CreateNumberSubstitution","dwrite/IDWriteFactory::CreateNumberSubstitution"]
old-location: directwrite\IDWriteFactory_CreateNumberSubstitution.htm
tech.root: DirectWrite
ms.assetid: a2778bfd-c721-44e8-ac0a-79aaa2b323a8
ms.date: 12/05/2018
ms.keywords: CreateNumberSubstitution, CreateNumberSubstitution method [Direct Write], CreateNumberSubstitution method [Direct Write],IDWriteFactory interface, IDWriteFactory interface [Direct Write],CreateNumberSubstitution method, IDWriteFactory.CreateNumberSubstitution, IDWriteFactory::CreateNumberSubstitution, directwrite.IDWriteFactory_CreateNumberSubstitution, dwrite/IDWriteFactory::CreateNumberSubstitution
f1_keywords:
- dwrite/IDWriteFactory.CreateNumberSubstitution
dev_langs:
- c++
req.header: dwrite.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dwrite.lib
req.dll: Dwrite.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- dwrite.dll
api_name:
- IDWriteFactory.CreateNumberSubstitution
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDWriteFactory::CreateNumberSubstitution


## -description


 Creates a number substitution object using a locale name,
     substitution method, and an indicator  whether to ignore user overrides (use NLS
     defaults for the given culture instead).


## -parameters




### -param substitutionMethod [in]

Type: <b><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_number_substitution_method">DWRITE_NUMBER_SUBSTITUTION_METHOD</a></b>

A value that specifies how to apply number substitution on digits and related punctuation.


### -param localeName [in]

Type: <b>const WCHAR*</b>

The name of the locale to be used in the <i>numberSubstitution</i> object.


### -param ignoreUserOverride [in]

Type: <b>BOOL</b>

A Boolean flag that indicates whether to ignore user overrides.


### -param numberSubstitution [out]

Type: <b><a href="/windows/win32/DirectWrite/idwritenumbersubstitution">IDWriteNumberSubstitution</a>**</b>

When this method returns, contains an address to  a pointer to the number substitution object created by this method.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="/windows/win32/api/dwrite/nn-dwrite-idwritefactory">IDWriteFactory</a>
 

 

