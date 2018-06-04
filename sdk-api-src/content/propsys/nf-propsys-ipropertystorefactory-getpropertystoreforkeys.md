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

# IPropertyStoreFactory::GetPropertyStoreForKeys


## -description


Gets an <a href="https://msdn.microsoft.com/library/windows/hardware/ff536954">IPropertyStore</a> object, given a set of property keys. This provides an alternative, possibly faster, method of getting an <b>IPropertyStore</b> object compared to calling <a href="shell.IPropertyStoreFactory_GetPropertyStore">IPropertyStoreFactory::GetPropertyStore</a>.


## -parameters




### -param rgKeys [in]

Type: <b>const <a href="shell.PROPERTYKEY">PROPERTYKEY</a>*</b>

A pointer to an array of <a href="shell.PROPERTYKEY">PROPERTYKEY</a> structures.


### -param cKeys [in]

Type: <b>UINT</b>

The number of <a href="shell.PROPERTYKEY">PROPERTYKEY</a> structures in the array pointed to by <i>rgKeys</i>.


### -param flags [in]

Type: <b><a href="shell.GETPROPERTYSTOREFLAGS">GETPROPERTYSTOREFLAGS</a></b>


<a href="shell.GETPROPERTYSTOREFLAGS">GETPROPERTYSTOREFLAGS</a> values that modify the store that is returned.


### -param riid [in]

Type: <b>REFIID</b>

A reference to IID of the object to create.


### -param ppv [out]

Type: <b>void**</b>


          When this method returns, contains the address of an <a href="https://msdn.microsoft.com/library/windows/hardware/ff536954">IPropertyStore</a> interface pointer.
        


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks




        It is recommended that you use the IID_PPV_ARGS macro, defined in Objbase.h, to package the <i>riid</i> and <i>ppv</i> parameters. This macro provides the correct IID based on the interface pointed to by the value in <i>ppv</i>, which eliminates the possibility of a coding error.
      



