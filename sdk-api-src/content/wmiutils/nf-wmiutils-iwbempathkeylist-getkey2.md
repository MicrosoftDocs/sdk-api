---
UID: NF:wmiutils.IWbemPathKeyList.GetKey2
title: IWbemPathKeyList::GetKey2
author: windows-sdk-content
description: The IWbemPathKeyList::GetKey2 method retrieves a key name or value, and returns the value as a VARIANT. A key is indexed from 0 (zero), but the key order is not significant.
old-location: wmi\iwbempathkeylist_getkey2.htm
tech.root: WmiSdk
ms.assetid: 009a1778-d2e3-4202-a640-60a55d5f3f8d
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetKey2, GetKey2 method [Windows Management Instrumentation], GetKey2 method [Windows Management Instrumentation],IWbemPathKeyList interface, IWbemPathKeyList interface [Windows Management Instrumentation],GetKey2 method, IWbemPathKeyList.GetKey2, IWbemPathKeyList::GetKey2, _hmm_iwbempathkeylist_getkey2, wmi.iwbempathkeylist_getkey2, wmiutils/IWbemPathKeyList::GetKey2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wmiutils.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wbemuuid.lib
req.dll: Wmiutils.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmiutils.dll
api_name:
 - IWbemPathKeyList.GetKey2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- wmiutils.h
: 
- IWbemPathKeyList.GetKey2
: 
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


### -param pKeyValue [out]

Pointer to a variant that contains the key value.


### -param puApparentCimType [out]

Pointer to a long integer that is set to the CIM type.


## -returns



This method returns an <b>HRESULT</b> that indicates the status of the method call.




## -remarks



This method can be used to determine how big a buffer is needed by passing in a <b>NULL</b> pointer for the buffer and setting its size parameter to 0 (zero). When returned, the buffer size parameter indicates the size buffer that is needed for the string and its <b>NULL</b> terminator.




## -see-also




<a href="https://msdn.microsoft.com/71b2597b-d82a-439d-b0b7-af76aefea6a2">IWbemPath</a>



<a href="https://msdn.microsoft.com/5b188426-9d7f-4e87-9eed-ce80e5d93c30">IWbemPathKeyList</a>



<a href="https://msdn.microsoft.com/98b3a8e6-f2cf-4a39-91f9-eb20e397e54e">IWbemPathKeyList::GetKey</a>
 

 

