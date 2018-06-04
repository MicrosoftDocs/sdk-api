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

# IWbemObjectAccess::ReadPropertyValue


## -description


The <b>ReadPropertyValue</b> method returns a specified number of bytes of a property associated with a property handle. Use this method to read the value of a property that contains a string or to read a property that contains a value that is not 32 (<b>DWORD</b>) or 64 (<b>QWORD</b>) bits long.


## -parameters




### -param lHandle [in]

Integer that contains the handle identifying this property.


### -param lBufferSize [in]

Integer that contains the buffer size.


### -param plNumBytes [out]

Pointer to an integer used to return the number of bytes read.


### -param aData [out]

Pointer to an array used to return the property data.


## -returns



This method returns <b>WBEM_S_NO_ERROR</b> if successful; otherwise, this method returns an <b>HRESULT</b> with one of the following values.




## -remarks



String data is returned as <b>null</b>-terminated <b>WCHAR</b> data.




## -see-also




<a href="https://msdn.microsoft.com/1025ae50-870f-4d38-8e83-3c6b628315c6">IWbemObjectAccess</a>
 

 

