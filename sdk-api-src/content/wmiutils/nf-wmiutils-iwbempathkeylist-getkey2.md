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

# IWbemPathKeyList::GetKey2


## -description


The 
<b>IWbemPathKeyList::GetKey2</b> method retrieves a key name or value, and  returns the value as a <b>VARIANT</b>. A key is indexed from 0 (zero), but the key order  is not significant.


## -parameters




### -param uKeyIx [in]

Key index begins at 0 (zero).


### -param uFlags [in]

Reserved. Must be 0 (zero).


### -param puNameBufSize [in, out]

Caller sets this parameter to the number of characters that the name buffer can hold. When successful, this is set to the number of characters that are copied into the buffer—including the terminating <b>NULL</b>.


### -param pszKeyName [out]

Buffer into which the name is copied. Because not all keys have a name, this parameter value is <b>NULL</b> for an implicit key.


### -param pKeyValue




### -param puApparentCimType [out]

Pointer to a long integer that is set to the CIM type.


#### - pKeyVal [out]

Pointer to a variant that contains the key value.


## -returns



This method returns an <b>HRESULT</b> that indicates the status of the method call.




## -remarks



This method can be used to determine how big a buffer is needed by passing in a <b>NULL</b> pointer for the buffer and setting its size parameter to 0 (zero). When returned, the buffer size parameter indicates the size buffer that is needed for the string and its <b>NULL</b> terminator.




## -see-also




<a href="https://msdn.microsoft.com/71b2597b-d82a-439d-b0b7-af76aefea6a2">IWbemPath</a>



<a href="https://msdn.microsoft.com/5b188426-9d7f-4e87-9eed-ce80e5d93c30">IWbemPathKeyList</a>



<a href="https://msdn.microsoft.com/98b3a8e6-f2cf-4a39-91f9-eb20e397e54e">IWbemPathKeyList::GetKey</a>
 

 

