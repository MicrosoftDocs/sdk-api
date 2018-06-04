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

# _ADSPROPINITPARAMS structure


## -description


The <b>ADSPROPINITPARAMS</b> structure is used with the <a href="https://msdn.microsoft.com/dcc4ea8f-6924-4e26-a675-ce326f35933c">ADsPropGetInitInfo</a> function to obtain object data that a display specifier applies to.


## -struct-fields




### -field dwSize

The size, in bytes, of the <b>ADSPROPINITPARAMS</b> structure. Set this value before calling <a href="https://msdn.microsoft.com/dcc4ea8f-6924-4e26-a675-ce326f35933c">ADsPropGetInitInfo</a>.


### -field dwFlags

Reserved.


### -field hr

Contains an <b>HRESULT</b> value that specifies the result of the bind/get operation. If this value does not equal <b>S_OK</b>, then the remaining structure members are not initialized and should be ignored.


### -field pDsObj

Pointer to an <a href="https://msdn.microsoft.com/bc4f8920-2881-4393-bb01-ed837c3db6ad">IDirectoryObject</a> interface that represents the directory object that the display specifier applies to. Do not release this interface.


### -field pwzCN

Pointer to a null-terminated Unicode string that contains the common name of the directory object.


### -field pWritableAttrs

Pointer to an <a href="https://msdn.microsoft.com/a2b97a52-4b8b-4491-8798-72a161903422">ADS_ATTR_INFO</a> structure that contains attribute data for the directory object.


## -remarks



The <a href="https://msdn.microsoft.com/dcc4ea8f-6924-4e26-a675-ce326f35933c">ADsPropGetInitInfo</a> function allocates memory  for the <b>pwzCN</b> and <b>pWritableAttrs</b> members. This memory is freed by the system after all display specifier objects are destroyed. The reference count for the interface pointer in <b>pDsObj</b> is not incremented by calling <b>ADsPropGetInitInfo</b>, so the interface must not be released by the caller.




## -see-also




<a href="https://msdn.microsoft.com/a2b97a52-4b8b-4491-8798-72a161903422">ADS_ATTR_INFO</a>



<a href="https://msdn.microsoft.com/dcc4ea8f-6924-4e26-a675-ce326f35933c">ADsPropGetInitInfo</a>



<a href="https://msdn.microsoft.com/bc4f8920-2881-4393-bb01-ed837c3db6ad">IDirectoryObject</a>
 

 

