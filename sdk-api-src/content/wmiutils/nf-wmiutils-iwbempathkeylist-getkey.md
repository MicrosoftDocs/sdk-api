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

# IWbemPathKeyList::GetKey


## -description


The 
<b>IWbemPathKeyList::GetKey</b> method retrieves a key's name or value. Keys are indexed from 0 (zero), though the order of the keys is not significant.


## -parameters




### -param uKeyIx [in]

Key index beginning at 0 (zero).


### -param uFlags [in]

Reserved. Must be 0 (zero).


### -param puNameBufSize [in, out]

Caller sets this to the number of characters that the name buffer can hold. Upon success, this is set to the number of characters copied into the buffer including the terminating <b>NULL</b>.


### -param pszKeyName [in, out]

Buffer into which the name is to be copied. Because not all keys have a name, this parameter value would be <b>NULL</b> for an implicit key.


### -param puKeyValBufSize [in, out]

Caller sets this to the number of characters that the value buffer can hold. Upon success, this is set to the number of characters copied into the buffer including the <b>NULL</b> terminator.


### -param pKeyVal [in, out]

Buffer where data is to be copied.


### -param puApparentCimType [in, out]

Pointer to a long which is set to the CIM type.


## -returns



This method returns an <b>HRESULT</b> indicating the status of the method call.




## -remarks



It is a recommended practice to determine how big a buffer is needed by calling this method, passing in a <b>NULL</b> pointer for the buffer, and setting its size parameter to 0 (zero). Upon return, the size parameter of the buffer indicates how large of a buffer is needed for the string and its <b>NULL</b> terminator. Then you can call the method to get the buffer value.




## -see-also




<a href="https://msdn.microsoft.com/71b2597b-d82a-439d-b0b7-af76aefea6a2">IWbemPath</a>



<a href="https://msdn.microsoft.com/5b188426-9d7f-4e87-9eed-ce80e5d93c30">IWbemPathKeyList</a>



<a href="https://msdn.microsoft.com/009a1778-d2e3-4202-a640-60a55d5f3f8d">IWbemPathKeyList::GetKey2</a>
 

 

