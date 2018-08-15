---
UID: NF:azroles.IAzApplication3.CreateScope2
title: IAzApplication3::CreateScope2
author: windows-sdk-content
description: Creates a new IAzScope2 object with the specified name.
old-location: security\iazapplication3_createscope2.htm
old-project: secauthz
ms.assetid: f1e8bfe6-e074-4e9e-80f8-bcb8bd90f824
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: CreateScope2, CreateScope2 method [Security], CreateScope2 method [Security],IAzApplication3 interface, IAzApplication3 interface [Security],CreateScope2 method, IAzApplication3.CreateScope2, IAzApplication3::CreateScope2, azroles/IAzApplication3::CreateScope2, security.iazapplication3_createscope2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: azroles.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: AZ_PROP_CONSTANTS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Azroles.dll
api_name:
 - IAzApplication3.CreateScope2
product: Windows
targetos: Windows
req.lib: 
req.dll: Azroles.dll
req.irql: 
---

# IAzApplication3::CreateScope2


## -description


The <b>CreateScope2</b> method creates a new <a href="https://msdn.microsoft.com/536c563e-7a6b-480d-9e83-1d7cc90a795d">IAzScope2</a> object with the specified name.


## -parameters




### -param bstrScopeName [in]

A string that contains the name of the new <a href="https://msdn.microsoft.com/536c563e-7a6b-480d-9e83-1d7cc90a795d">IAzScope2</a> object.


### -param ppScope2 [out]

The address of a pointer to the <a href="https://msdn.microsoft.com/536c563e-7a6b-480d-9e83-1d7cc90a795d">IAzScope2</a> object that this method creates.

When you have finished using this <a href="https://msdn.microsoft.com/536c563e-7a6b-480d-9e83-1d7cc90a795d">IAzScope2</a> object, release it by calling the <a href="https://msdn.microsoft.com/en-us/library/ms682317(v=VS.85).aspx">IUnknown::Release</a> method.


## -returns



 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.



