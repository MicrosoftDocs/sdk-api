---
UID: NF:propsys.IPropertyStoreFactory.GetPropertyStore
title: IPropertyStoreFactory::GetPropertyStore
author: windows-sdk-content
description: Gets an IPropertyStore object that corresponds to the supplied flags.
old-location: properties\IPropertyStoreFactory_GetPropertyStore.htm
tech.root: properties
ms.assetid: 80cc20e1-88e2-4dee-a0fb-d75fffdfc097
ms.author: windowssdkdev
ms.date: 09/07/2018
ms.keywords: GetPropertyStore, GetPropertyStore method [Windows Properties], GetPropertyStore method [Windows Properties],IPropertyStoreFactory interface, IPropertyStoreFactory interface [Windows Properties],GetPropertyStore method, IPropertyStoreFactory.GetPropertyStore, IPropertyStoreFactory::GetPropertyStore, _shell_IPropertyStoreFactory_GetPropertyStore, properties.IPropertyStoreFactory_GetPropertyStore, propsys/IPropertyStoreFactory::GetPropertyStore, shell.IPropertyStoreFactory_GetPropertyStore
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: propsys.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Propsys.idl
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
 - Propsys.h
api_name:
 - IPropertyStoreFactory.GetPropertyStore
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPropertyStoreFactory::GetPropertyStore


## -description


Gets an <a href="https://msdn.microsoft.com/en-us/library/Bb761474(v=VS.85).aspx">IPropertyStore</a> object that corresponds to the supplied flags.


## -parameters




### -param flags [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb762582(v=VS.85).aspx">GETPROPERTYSTOREFLAGS</a></b>


<a href="https://msdn.microsoft.com/en-us/library/Bb762582(v=VS.85).aspx">GETPROPERTYSTOREFLAGS</a> values that modify the store that is returned.


### -param pUnkFactory [in]

Type: <b><a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>*</b>

Optional. A pointer to the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> of an object that implements <a href="https://msdn.microsoft.com/90502b4a-dc0a-4077-83d7-e9f5445ba69b">ICreateObject</a>. If <i>pUnkFactory</i> is provided, this method can create the handler instance using <b>ICreateObject</b> rather than <a href="https://msdn.microsoft.com/7295a55b-12c7-4ed0-a7a4-9ecee16afdec">CoCreateInstance</a>, if implemented. The reason to provide <i>pUnkFactory</i> is usually to create the handler in a different process. However, for most users, passing <b>NULL</b> in this parameter is sufficient.


### -param riid [in]

Type: <b>REFIID</b>

A reference to IID of the object to create.


### -param ppv [out]

Type: <b>void**</b>

When this method returns, contains the address of an <a href="https://msdn.microsoft.com/en-us/library/Bb761474(v=VS.85).aspx">IPropertyStore</a> interface pointer.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



It is recommended that you use the IID_PPV_ARGS macro, defined in Objbase.h, to package the <i>riid</i> and <i>ppv</i> parameters. This macro provides the correct IID based on the interface pointed to by the value in <i>ppv</i>, which eliminates the possibility of a coding error.



