---
UID: NF:oleauto.QueryPathOfRegTypeLib
title: QueryPathOfRegTypeLib function
author: windows-driver-content
description: Retrieves the path of a registered type library.
old-location: automat\querypathofregtypelib.htm
old-project: automat
ms.assetid: a71dc182-2fbf-48bd-9c9a-c662b9b0a6ec
ms.author: windowsdriverdev
ms.date: 5/4/2018
ms.keywords: QueryPathOfRegTypeLib, QueryPathOfRegTypeLib function [Automation], _oa96_QueryPathOfRegTypeLib, automat.querypathofregtypelib, oleauto/QueryPathOfRegTypeLib
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: oleauto.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: REGKIND
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	OleAut32.dll
api_name:
-	QueryPathOfRegTypeLib
product: Windows
targetos: Windows
req.lib: OleAut32.lib
req.dll: OleAut32.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# QueryPathOfRegTypeLib function


## -description


Retrieves the path of a registered type library.


## -parameters




### -param guid

The GUID of the library.




### -param wMaj

The major version number of the library.


### -param wMin

The minor version number of the library.


### -param lcid

The national language code for the library.


### -param lpbstrPathName [out]

The type library name.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Returns the fully qualified file name that is specified for the type library in the registry. The caller allocates the BSTR that is passed in, and must free it after use.




