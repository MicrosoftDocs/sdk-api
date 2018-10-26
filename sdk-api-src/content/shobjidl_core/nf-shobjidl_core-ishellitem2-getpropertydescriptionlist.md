---
UID: NF:shobjidl_core.IShellItem2.GetPropertyDescriptionList
title: IShellItem2::GetPropertyDescriptionList
author: windows-sdk-content
description: Gets a property description list object given a reference to a property key.
old-location: shell\IShellItem2_GetPropertyDescriptionList.htm
tech.root: shell
ms.assetid: 443b95c9-0a9e-4ad5-8774-ad3b1b51c136
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: GetPropertyDescriptionList, GetPropertyDescriptionList method [Windows Shell], GetPropertyDescriptionList method [Windows Shell],IShellItem2 interface, IShellItem2 interface [Windows Shell],GetPropertyDescriptionList method, IShellItem2.GetPropertyDescriptionList, IShellItem2::GetPropertyDescriptionList, _shell_IShellItem2_GetPropertyDescriptionList, shell.IShellItem2_GetPropertyDescriptionList, shobjidl_core/IShellItem2::GetPropertyDescriptionList
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
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
 - shobjidl_core.h
api_name:
 - IShellItem2.GetPropertyDescriptionList
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IShellItem2::GetPropertyDescriptionList


## -description


Gets a property description list object given a reference to a property key.


## -parameters




### -param keyType [in]

Type: <b>REFPROPERTYKEY</b>

A reference to a <a href="https://msdn.microsoft.com/3f5f31af-f040-443b-9045-9761055381ea">PROPERTYKEY</a> structure.


### -param riid [in]

Type: <b>REFIID</b>

A reference to a desired IID.


### -param ppv [out]

Type: <b>void**</b>

Contains the address of an <a href="https://msdn.microsoft.com/e0530195-27da-4df7-884f-518e905f3c0e">IPropertyDescriptionList</a> interface pointer.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



