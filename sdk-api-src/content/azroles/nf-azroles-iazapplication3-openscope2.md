---
UID: NF:azroles.IAzApplication3.OpenScope2
title: IAzApplication3::OpenScope2
author: windows-driver-content
description: Opens an IAzScope2 object with the specified name.
old-location: security\iazapplication3_openscope2.htm
old-project: SecAuthZ
ms.assetid: 1ea9f12e-d00d-4ccd-bfd4-21027610e681
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: IAzApplication3 interface [Security],OpenScope2 method, IAzApplication3.OpenScope2, IAzApplication3::OpenScope2, OpenScope2, OpenScope2 method [Security], OpenScope2 method [Security],IAzApplication3 interface, azroles/IAzApplication3::OpenScope2, security.iazapplication3_openscope2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: azroles.h
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
req.typenames: AZ_PROP_CONSTANTS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Azroles.dll
api_name:
-	IAzApplication3.OpenScope2
product: Windows
targetos: Windows
req.lib: 
req.dll: Azroles.dll
req.irql: 
---

# IAzApplication3::OpenScope2


## -description


The <b>OpenScope2</b> method opens an <a href="https://msdn.microsoft.com/536c563e-7a6b-480d-9e83-1d7cc90a795d">IAzScope2</a> object with the specified name.


## -parameters




### -param bstrScopeName [in]

A string that contains the name of the <a href="https://msdn.microsoft.com/536c563e-7a6b-480d-9e83-1d7cc90a795d">IAzScope2</a> object to open.


### -param ppScope2 [out]

The address of a pointer to the <a href="https://msdn.microsoft.com/536c563e-7a6b-480d-9e83-1d7cc90a795d">IAzScope2</a> object that this method opens.

When you have finished using the <a href="https://msdn.microsoft.com/536c563e-7a6b-480d-9e83-1d7cc90a795d">IAzScope2</a> object, release it by calling the <a href="_com_iunknown_release">IUnknown::Release</a> method.


## -returns



 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.



