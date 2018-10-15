---
UID: NF:shellapi.AssocCreateForClasses
title: AssocCreateForClasses function
author: windows-sdk-content
description: Retrieves an object that implements an IQueryAssociations interface.
old-location: shell\AssocCreateForClasses.htm
tech.root: shell
ms.assetid: 43257507-dd5e-4622-8445-c132187fd1e5
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: AssocCreateForClasses, AssocCreateForClasses function [Windows Shell], _shell_AssocCreateForClasses, shell.AssocCreateForClasses, shellapi/AssocCreateForClasses
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: shellapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
 - Windows.Storage.dll
 - API-MS-Win-Shell-Associations-L1-1-0.dll
api_name:
 - AssocCreateForClasses
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# AssocCreateForClasses function


## -description


Retrieves an object that implements an <a href="https://msdn.microsoft.com/8edb99d3-5860-4d78-a750-1df34cdfc313">IQueryAssociations</a> interface.


## -parameters




### -param rgClasses [in]

Type: <b>const <a href="https://msdn.microsoft.com/1d1a963f-7ebb-4ba6-9a97-795c8ef11ae4">ASSOCIATIONELEMENT</a>*</b>

A pointer to an array of <a href="https://msdn.microsoft.com/1d1a963f-7ebb-4ba6-9a97-795c8ef11ae4">ASSOCIATIONELEMENT</a> structures.


### -param cClasses [in]

Type: <b>ULONG</b>

The number of elements in the array pointed to by <i>rgClasses</i>.


### -param riid [in]

Type: <b>REFIID</b>

Reference to the desired IID, normally IID_IQueryAssociations.


### -param ppv [out]

Type: <b>void**</b>

When this method returns, contains the interface pointer requested in <i>riid</i>. This is normally <a href="https://msdn.microsoft.com/8edb99d3-5860-4d78-a750-1df34cdfc313">IQueryAssociations</a>.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



For systems earlier than Windows Vista, use the <a href="https://msdn.microsoft.com/33099e0e-73e3-4047-804f-765a59e42e3f">AssocCreate</a> function.



