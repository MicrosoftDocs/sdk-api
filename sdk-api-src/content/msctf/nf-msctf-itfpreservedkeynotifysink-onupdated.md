---
UID: NF:msctf.ITfPreservedKeyNotifySink.OnUpdated
title: ITfPreservedKeyNotifySink::OnUpdated (msctf.h)
description: ITfPreservedKeyNotifySink::OnUpdated method
helpviewer_keywords: ["ITfPreservedKeyNotifySink interface [Text Services Framework]","OnUpdated method","ITfPreservedKeyNotifySink.OnUpdated","ITfPreservedKeyNotifySink::OnUpdated","OnUpdated","OnUpdated method [Text Services Framework]","OnUpdated method [Text Services Framework]","ITfPreservedKeyNotifySink interface","_tsf_itfpreservedkeynotifysink_onupdated_ref","msctf/ITfPreservedKeyNotifySink::OnUpdated","tsf.itfpreservedkeynotifysink_onupdated"]
old-location: tsf\itfpreservedkeynotifysink_onupdated.htm
tech.root: TSF
ms.assetid: 50654da7-60ee-4038-a02a-1055445f1e5d
ms.date: 12/05/2018
ms.keywords: ITfPreservedKeyNotifySink interface [Text Services Framework],OnUpdated method, ITfPreservedKeyNotifySink.OnUpdated, ITfPreservedKeyNotifySink::OnUpdated, OnUpdated, OnUpdated method [Text Services Framework], OnUpdated method [Text Services Framework],ITfPreservedKeyNotifySink interface, _tsf_itfpreservedkeynotifysink_onupdated_ref, msctf/ITfPreservedKeyNotifySink::OnUpdated, tsf.itfpreservedkeynotifysink_onupdated
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msctf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfPreservedKeyNotifySink::OnUpdated
 - msctf/ITfPreservedKeyNotifySink::OnUpdated
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msctf.dll
api_name:
 - ITfPreservedKeyNotifySink.OnUpdated
---

# ITfPreservedKeyNotifySink::OnUpdated


## -description

Called when a key is preserved, unpreserved, or when a preserved key description changes.

## -parameters

### -param pprekey [in]

Pointer to a <a href="/windows/desktop/api/msctf/ns-msctf-tf_preservedkey">TF_PRESERVEDKEY</a> structure that contains data about the key.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

To determine if the key is unpreserved, call <a href="/windows/desktop/api/msctf/nf-msctf-itfkeystrokemgr-ispreservedkey">ITfKeystrokeMgr::IsPreservedKey</a>, passing <i>pprekey</i>. If the key is not found, it is unpreserved. If the key is found, it is either preserved or the description has changed. Unless you keep track of the current key description and compare the previous description with the current description in response to this notification, there is no way to determine if this notification is in response to a key preserved or the description changed.

## -see-also

<a href="/windows/desktop/api/msctf/nf-msctf-itfkeystrokemgr-preservekey">ITfKeystrokeMgr::PreserveKey
      </a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfkeystrokemgr-setpreservedkeydescription">ITfKeystrokeMgr::SetPreservedKeyDescription
      </a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfkeystrokemgr-unpreservekey">ITfKeystrokeMgr::UnpreserveKey
      </a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfpreservedkeynotifysink">ITfPreservedKeyNotifySink</a>



<a href="/windows/desktop/api/msctf/ns-msctf-tf_preservedkey">TF_PRESERVEDKEY
      </a>