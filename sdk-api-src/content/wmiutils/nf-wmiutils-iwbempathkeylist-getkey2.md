---
UID: NF:wmiutils.IWbemPathKeyList.GetKey2
title: IWbemPathKeyList::GetKey2 (wmiutils.h)
description: The IWbemPathKeyList::GetKey2 method retrieves a key name or value, and returns the value as a VARIANT. A key is indexed from 0 (zero), but the key order is not significant.
helpviewer_keywords: ["GetKey2","GetKey2 method [Windows Management Instrumentation]","GetKey2 method [Windows Management Instrumentation]","IWbemPathKeyList interface","IWbemPathKeyList interface [Windows Management Instrumentation]","GetKey2 method","IWbemPathKeyList.GetKey2","IWbemPathKeyList::GetKey2","_hmm_iwbempathkeylist_getkey2","wmi.iwbempathkeylist_getkey2","wmiutils/IWbemPathKeyList::GetKey2"]
old-location: wmi\iwbempathkeylist_getkey2.htm
tech.root: wmi
ms.assetid: 009a1778-d2e3-4202-a640-60a55d5f3f8d
ms.date: 12/05/2018
ms.keywords: GetKey2, GetKey2 method [Windows Management Instrumentation], GetKey2 method [Windows Management Instrumentation],IWbemPathKeyList interface, IWbemPathKeyList interface [Windows Management Instrumentation],GetKey2 method, IWbemPathKeyList.GetKey2, IWbemPathKeyList::GetKey2, _hmm_iwbempathkeylist_getkey2, wmi.iwbempathkeylist_getkey2, wmiutils/IWbemPathKeyList::GetKey2
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWbemPathKeyList::GetKey2
 - wmiutils/IWbemPathKeyList::GetKey2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmiutils.dll
api_name:
 - IWbemPathKeyList.GetKey2
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

<a href="/windows/desktop/api/wmiutils/nn-wmiutils-iwbempath">IWbemPath</a>



<a href="/windows/desktop/api/wmiutils/nn-wmiutils-iwbempathkeylist">IWbemPathKeyList</a>



<a href="/windows/desktop/api/wmiutils/nf-wmiutils-iwbempathkeylist-getkey">IWbemPathKeyList::GetKey</a>