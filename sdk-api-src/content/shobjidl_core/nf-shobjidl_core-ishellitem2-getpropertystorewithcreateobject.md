---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IShellItem2::GetPropertyStoreWithCreateObject


## -description


Uses the specified <a href="https://msdn.microsoft.com/90502b4a-dc0a-4077-83d7-e9f5445ba69b">ICreateObject</a> instead of <a href="https://msdn.microsoft.com/7295a55b-12c7-4ed0-a7a4-9ecee16afdec">CoCreateInstance</a> to create an instance of the property handler associated with the Shell item on which this method is called. Most calling applications do not need to call this method, and can call <a href="https://msdn.microsoft.com/706b2551-a9b0-4368-babb-e54cea6d297e">IShellItem2::GetPropertyStore</a> instead.


## -parameters




### -param flags [in]

Type: <b><a href="https://msdn.microsoft.com/d3fde1b9-b19f-431d-9cea-bffc289ee683">GETPROPERTYSTOREFLAGS</a></b>

The <a href="https://msdn.microsoft.com/d3fde1b9-b19f-431d-9cea-bffc289ee683">GETPROPERTYSTOREFLAGS</a> constants that modify the property store object.


### -param punkCreateObject




### -param riid [in]

Type: <b>REFIID</b>

A reference to the IID of the object to be retrieved.


### -param ppv [out]

Type: <b>void**</b>

When this method returns, contains the address of the requested <a href="https://msdn.microsoft.com/library/windows/hardware/ff536954">IPropertyStore</a> interface pointer.


#### - punkFactory [in]

Type: <b><a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>*</b>

A pointer to a factory for low-rights creation of type <a href="https://msdn.microsoft.com/90502b4a-dc0a-4077-83d7-e9f5445ba69b">ICreateObject</a>.

                    

The method <a href="https://msdn.microsoft.com/72c56de7-4c04-4bcf-b6bb-6e41d12b68a3">CreateObject</a> creates an instance of a COM object. The implementation of <b>IShellItem2::GetPropertyStoreWithCreateObject</b> uses <b>CreateObject</b> instead of <a href="https://msdn.microsoft.com/7295a55b-12c7-4ed0-a7a4-9ecee16afdec">CoCreateInstance</a> to create the property handler, which is a Shell extension, for a given file type. The property handler provides many of the important properties in the property store that this method returns.

This method is useful only if the <a href="https://msdn.microsoft.com/90502b4a-dc0a-4077-83d7-e9f5445ba69b">ICreateObject</a> object is created in a separate process (as a LOCALSERVER instead of an INPROCSERVER), and also if this other process has lower rights than the process calling <b>IShellItem2::GetPropertyStoreWithCreateObject</b>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<div class="alert"><b>Note</b>  When this method is called on a property store for a file, that file is held open for the lifetime of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff536954">IPropertyStore</a> object.</div>
<div> </div>


