---
UID: NF:shlwapi.AssocCreate
title: AssocCreate function
author: windows-driver-content
description: Returns a pointer to an IQueryAssociations object.
old-location: shell\AssocCreate.htm
old-project: shell
ms.assetid: 33099e0e-73e3-4047-804f-765a59e42e3f
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: AssocCreate, AssocCreate function [Windows Shell], _win32_AssocCreate, shell.AssocCreate, shlwapi/AssocCreate
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: URL_SCHEME
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Shlwapi.dll
-	API-MS-Win-shlwapi-Winrt-storage-l1-1-0.dll
-	api-ms-win-shlwapi-winrt-storage-l1-1-1.dll
api_name:
-	AssocCreate
product: Windows
targetos: Windows
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 5.0 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# AssocCreate function


## -description


Returns a pointer to an <a href="https://msdn.microsoft.com/8edb99d3-5860-4d78-a750-1df34cdfc313">IQueryAssociations</a> object.


## -parameters




### -param clsid [in]

Type: <b>CLSID</b>

The CLSID of the object that exposes the interface. This parameter must be set to CLSID_QueryAssociations, which is defined in Shlguid.h.


### -param riid [in]

Type: <b>REFIID</b>

Reference to the IID IID_IQueryAssociations, which is defined in Shlguid.h.


### -param ppv [out]

Type: <b>void*</b>

When this method returns, contains the <a href="https://msdn.microsoft.com/8edb99d3-5860-4d78-a750-1df34cdfc313">IQueryAssociations</a> interface pointer requested in <i>riid</i>.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



As of Windows Vista, <a href="https://msdn.microsoft.com/43257507-dd5e-4622-8445-c132187fd1e5">AssocCreateForClasses</a> is preferred to <b>AssocCreate</b>.



