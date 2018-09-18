---
UID: NF:shobjidl_core.IShellItem2.GetPropertyStoreWithCreateObject
title: IShellItem2::GetPropertyStoreWithCreateObject
author: windows-sdk-content
description: Uses the specified ICreateObject instead of CoCreateInstance to create an instance of the property handler associated with the Shell item on which this method is called.
old-location: shell\IShellItem2_GetPropertyStoreWithCreateObject.htm
tech.root: shell
ms.assetid: 6a90ea62-e4d7-4876-802a-9c1f6c296714
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: GetPropertyStoreWithCreateObject, GetPropertyStoreWithCreateObject method [Windows Shell], GetPropertyStoreWithCreateObject method [Windows Shell],IShellItem2 interface, IShellItem2 interface [Windows Shell],GetPropertyStoreWithCreateObject method, IShellItem2.GetPropertyStoreWithCreateObject, IShellItem2::GetPropertyStoreWithCreateObject, _shell_IShellItem2_GetPropertyStoreWithCreateObject, shell.IShellItem2_GetPropertyStoreWithCreateObject, shobjidl_core/IShellItem2::GetPropertyStoreWithCreateObject
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
 - IShellItem2.GetPropertyStoreWithCreateObject
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IShellItem2::GetPropertyStoreWithCreateObject


## -description


Uses the specified <a href="https://msdn.microsoft.com/90502b4a-dc0a-4077-83d7-e9f5445ba69b">ICreateObject</a> instead of <a href="https://msdn.microsoft.com/7295a55b-12c7-4ed0-a7a4-9ecee16afdec">CoCreateInstance</a> to create an instance of the property handler associated with the Shell item on which this method is called. Most calling applications do not need to call this method, and can call <a href="https://msdn.microsoft.com/706b2551-a9b0-4368-babb-e54cea6d297e">IShellItem2::GetPropertyStore</a> instead.


## -parameters




### -param flags [in]

Type: <b><a href="https://msdn.microsoft.com/d3fde1b9-b19f-431d-9cea-bffc289ee683">GETPROPERTYSTOREFLAGS</a></b>

The <a href="https://msdn.microsoft.com/d3fde1b9-b19f-431d-9cea-bffc289ee683">GETPROPERTYSTOREFLAGS</a> constants that modify the property store object.


### -param punkCreateObject

TBD


### -param riid [in]

Type: <b>REFIID</b>

A reference to the IID of the object to be retrieved.


### -param ppv [out]

Type: <b>void**</b>

When this method returns, contains the address of the requested <a href="https://msdn.microsoft.com/e995aaa1-d4c9-475f-b1fa-b9123cd5b653">IPropertyStore</a> interface pointer.


#### - punkFactory [in]

Type: <b><a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>*</b>

A pointer to a factory for low-rights creation of type <a href="https://msdn.microsoft.com/90502b4a-dc0a-4077-83d7-e9f5445ba69b">ICreateObject</a>.

                    

The method <a href="https://msdn.microsoft.com/72c56de7-4c04-4bcf-b6bb-6e41d12b68a3">CreateObject</a> creates an instance of a COM object. The implementation of <b>IShellItem2::GetPropertyStoreWithCreateObject</b> uses <b>CreateObject</b> instead of <a href="https://msdn.microsoft.com/7295a55b-12c7-4ed0-a7a4-9ecee16afdec">CoCreateInstance</a> to create the property handler, which is a Shell extension, for a given file type. The property handler provides many of the important properties in the property store that this method returns.

This method is useful only if the <a href="https://msdn.microsoft.com/90502b4a-dc0a-4077-83d7-e9f5445ba69b">ICreateObject</a> object is created in a separate process (as a LOCALSERVER instead of an INPROCSERVER), and also if this other process has lower rights than the process calling <b>IShellItem2::GetPropertyStoreWithCreateObject</b>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<div class="alert"><b>Note</b>  When this method is called on a property store for a file, that file is held open for the lifetime of the <a href="https://msdn.microsoft.com/e995aaa1-d4c9-475f-b1fa-b9123cd5b653">IPropertyStore</a> object.</div>
<div> </div>


