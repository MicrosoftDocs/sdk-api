---
UID: NF:wmiutils.IWbemPathKeyList.GetKey
title: IWbemPathKeyList::GetKey (wmiutils.h)
description: The IWbemPathKeyList::GetKey method retrieves a key's name or value. Keys are indexed from 0 (zero), though the order of the keys is not significant.
helpviewer_keywords: ["GetKey","GetKey method [Windows Management Instrumentation]","GetKey method [Windows Management Instrumentation]","IWbemPathKeyList interface","IWbemPathKeyList interface [Windows Management Instrumentation]","GetKey method","IWbemPathKeyList.GetKey","IWbemPathKeyList::GetKey","_hmm_iwbempathkeylist_getkey","wmi.iwbempathkeylist_getkey","wmiutils/IWbemPathKeyList::GetKey"]
old-location: wmi\iwbempathkeylist_getkey.htm
tech.root: wmi
ms.assetid: 98b3a8e6-f2cf-4a39-91f9-eb20e397e54e
ms.date: 12/05/2018
ms.keywords: GetKey, GetKey method [Windows Management Instrumentation], GetKey method [Windows Management Instrumentation],IWbemPathKeyList interface, IWbemPathKeyList interface [Windows Management Instrumentation],GetKey method, IWbemPathKeyList.GetKey, IWbemPathKeyList::GetKey, _hmm_iwbempathkeylist_getkey, wmi.iwbempathkeylist_getkey, wmiutils/IWbemPathKeyList::GetKey
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
 - IWbemPathKeyList::GetKey
 - wmiutils/IWbemPathKeyList::GetKey
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
 - IWbemPathKeyList.GetKey
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

<a href="/windows/desktop/api/wmiutils/nn-wmiutils-iwbempath">IWbemPath</a>



<a href="/windows/desktop/api/wmiutils/nn-wmiutils-iwbempathkeylist">IWbemPathKeyList</a>



<a href="/windows/desktop/api/wmiutils/nf-wmiutils-iwbempathkeylist-getkey2">IWbemPathKeyList::GetKey2</a>