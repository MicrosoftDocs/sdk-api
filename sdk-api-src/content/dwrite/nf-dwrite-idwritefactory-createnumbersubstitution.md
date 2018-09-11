---
UID: NF:dwrite.IDWriteFactory.CreateNumberSubstitution
title: IDWriteFactory::CreateNumberSubstitution
author: windows-sdk-content
description: Creates a number substitution object using a locale name, substitution method, and an indicator whether to ignore user overrides (use NLS defaults for the given culture instead).
old-location: directwrite\IDWriteFactory_CreateNumberSubstitution.htm
tech.root: DirectWrite
ms.assetid: a2778bfd-c721-44e8-ac0a-79aaa2b323a8
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: CreateNumberSubstitution, CreateNumberSubstitution method [Direct Write], CreateNumberSubstitution method [Direct Write],IDWriteFactory interface, IDWriteFactory interface [Direct Write],CreateNumberSubstitution method, IDWriteFactory.CreateNumberSubstitution, IDWriteFactory::CreateNumberSubstitution, directwrite.IDWriteFactory_CreateNumberSubstitution, dwrite/IDWriteFactory::CreateNumberSubstitution
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteFactory::CreateNumberSubstitution


## -description


 Creates a number substitution object using a locale name,
     substitution method, and an indicator  whether to ignore user overrides (use NLS
     defaults for the given culture instead).


## -parameters




### -param substitutionMethod [in]

Type: <b><a href="https://msdn.microsoft.com/9702007f-ab08-4ad2-9fac-6482e17161ca">DWRITE_NUMBER_SUBSTITUTION_METHOD</a></b>

A value that specifies how to apply number substitution on digits and related punctuation.


### -param localeName [in]

Type: <b>const WCHAR*</b>

The name of the locale to be used in the <i>numberSubstitution</i> object.


### -param ignoreUserOverride [in]

Type: <b>BOOL</b>

A Boolean flag that indicates whether to ignore user overrides.


### -param numberSubstitution [out]

Type: <b><a href="https://msdn.microsoft.com/bf8caeea-6ede-4cd3-84f7-2e8314af50db">IDWriteNumberSubstitution</a>**</b>

When this method returns, contains an address to  a pointer to the number substitution object created by this method.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/73a85977-5c24-4abc-ad8c-1d0d6474bd7e">IDWriteFactory</a>
 

 

