---
UID: NF:shobjidl_core.IShellItem2.GetPropertyStoreForKeys
title: IShellItem2::GetPropertyStoreForKeys
author: windows-sdk-content
description: Gets property store object for specified property keys.
old-location: shell\IShellItem2_GetPropertyStoreForKeys.htm
old-project: shell
ms.assetid: 2d32ece8-4a68-4bf2-a1ee-bd94a2aa6fbd
ms.author: windowssdkdev
ms.date: 06/27/2018
ms.keywords: GetPropertyStoreForKeys, GetPropertyStoreForKeys method [Windows Shell], GetPropertyStoreForKeys method [Windows Shell],IShellItem2 interface, IShellItem2 interface [Windows Shell],GetPropertyStoreForKeys method, IShellItem2.GetPropertyStoreForKeys, IShellItem2::GetPropertyStoreForKeys, _shell_IShellItem2_GetPropertyStoreForKeys, shell.IShellItem2_GetPropertyStoreForKeys, shobjidl_core/IShellItem2::GetPropertyStoreForKeys
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IShellItem2.GetPropertyStoreForKeys
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IShellItem2::GetPropertyStoreForKeys


## -description


Gets property store object for specified property keys.


## -parameters




### -param rgKeys [in]

Type: <b>const <a href="https://msdn.microsoft.com/3f5f31af-f040-443b-9045-9761055381ea">PROPERTYKEY</a>*</b>

A pointer to an array of <a href="https://msdn.microsoft.com/3f5f31af-f040-443b-9045-9761055381ea">PROPERTYKEY</a> structures. Each structure contains a unique identifier for each property used in creating the property store.


### -param cKeys [in]

Type: <b>UINT</b>

The number of <a href="https://msdn.microsoft.com/3f5f31af-f040-443b-9045-9761055381ea">PROPERTYKEY</a> structures in the array pointed to by <i>rgKeys</i>.


### -param flags [in]

Type: <b><a href="https://msdn.microsoft.com/d3fde1b9-b19f-431d-9cea-bffc289ee683">GETPROPERTYSTOREFLAGS</a></b>

The <a href="https://msdn.microsoft.com/d3fde1b9-b19f-431d-9cea-bffc289ee683">GETPROPERTYSTOREFLAGS</a> constants that modify the property store object.


### -param riid [in]

Type: <b>REFIID</b>


          A reference to the IID of the object to be retrieved.
        


### -param ppv [out]

Type: <b>void**</b>


          When this method returns, contains the address of an <a href="https://msdn.microsoft.com/library/windows/hardware/ff536954">IPropertyStore</a> interface pointer.
        


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<div class="alert"><b>Note</b>  
        When this method is called on a property store for a file, that file is held open for the lifetime of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff536954">IPropertyStore</a> object.
      </div>
<div> </div>


