---
UID: NF:shellapi.AssocCreateForClasses
title: AssocCreateForClasses function (shellapi.h)
author: windows-sdk-content
description: Retrieves an object that implements an IQueryAssociations interface.
old-location: shell\AssocCreateForClasses.htm
tech.root: shell
ms.assetid: 43257507-dd5e-4622-8445-c132187fd1e5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: AssocCreateForClasses, AssocCreateForClasses function [Windows Shell], _shell_AssocCreateForClasses, shell.AssocCreateForClasses, shellapi/AssocCreateForClasses
ms.topic: function
f1_keywords: 
 - "shellapi/AssocCreateForClasses"
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# AssocCreateForClasses function


## -description


Retrieves an object that implements an <a href="https://docs.microsoft.com/windows/desktop/api/shlwapi/nn-shlwapi-iqueryassociations">IQueryAssociations</a> interface.


## -parameters




### -param rgClasses [in]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/api/shellapi/ns-shellapi-associationelement">ASSOCIATIONELEMENT</a>*</b>

A pointer to an array of <a href="https://docs.microsoft.com/windows/desktop/api/shellapi/ns-shellapi-associationelement">ASSOCIATIONELEMENT</a> structures.


### -param cClasses [in]

Type: <b>ULONG</b>

The number of elements in the array pointed to by <i>rgClasses</i>.


### -param riid [in]

Type: <b>REFIID</b>

Reference to the desired IID, normally IID_IQueryAssociations.


### -param ppv [out]

Type: <b>void**</b>

When this method returns, contains the interface pointer requested in <i>riid</i>. This is normally <a href="https://docs.microsoft.com/windows/desktop/api/shlwapi/nn-shlwapi-iqueryassociations">IQueryAssociations</a>.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



For systems earlier than Windows Vista, use the <a href="https://docs.microsoft.com/windows/desktop/api/shlwapi/nf-shlwapi-assoccreate">AssocCreate</a> function.



