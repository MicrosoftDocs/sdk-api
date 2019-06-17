---
UID: NF:shobjidl.IAccessibleObject.SetAccessibleName
title: IAccessibleObject::SetAccessibleName (shobjidl.h)
author: windows-sdk-content
description: Sets text that is retrieved by IAccessible::get_accName which accessibility tools use to obtain the Name Property of an object.
old-location: shell\IAccessibleObject_SetAccessibleName.htm
tech.root: shell
ms.assetid: 455d9434-1ea3-4a4e-ae4d-0952c895178c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAccessibleObject interface [Windows Shell],SetAccessibleName method, IAccessibleObject.SetAccessibleName, IAccessibleObject::SetAccessibleName, SetAccessibleName, SetAccessibleName method [Windows Shell], SetAccessibleName method [Windows Shell],IAccessibleObject interface, _shell_IAccessibleObject_SetAccessibleName, shell.IAccessibleObject_SetAccessibleName, shobjidl/IAccessibleObject::SetAccessibleName
ms.topic: method
f1_keywords: ["shobjidl/IAccessibleObject.SetAccessibleName"]
req.header: shobjidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shobjidl.h
api_name:
 - IAccessibleObject.SetAccessibleName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAccessibleObject::SetAccessibleName


## -description


Sets text that is retrieved by <a href="https://docs.microsoft.com/windows/desktop/api/oleacc/nf-oleacc-iaccessible-get_accname">IAccessible::get_accName</a> which accessibility tools use to obtain the Name Property of an object.



## -parameters




### -param pszName [in]

Type: <b>LPCWSTR</b>

A pointer to a null-terminated, Unicode string containing the name.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



