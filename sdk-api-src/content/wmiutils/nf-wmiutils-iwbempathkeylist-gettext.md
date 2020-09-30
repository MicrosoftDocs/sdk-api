---
UID: NF:wmiutils.IWbemPathKeyList.GetText
title: IWbemPathKeyList::GetText (wmiutils.h)
description: The IWbemPathKeyList::GetText method retrieves the key list as text.
helpviewer_keywords: ["GetText","GetText method [Windows Management Instrumentation]","GetText method [Windows Management Instrumentation]","IWbemPathKeyList interface","IWbemPathKeyList interface [Windows Management Instrumentation]","GetText method","IWbemPathKeyList.GetText","IWbemPathKeyList::GetText","WBEMPATH_QUOTEDTEXT","WBEMPATH_TEXT","_hmm_iwbempathkeylist_gettext","wmi.iwbempathkeylist_gettext","wmiutils/IWbemPathKeyList::GetText"]
old-location: wmi\iwbempathkeylist_gettext.htm
tech.root: wmi
ms.assetid: 01c69709-be6e-4a58-849d-76f9d4e3c196
ms.date: 12/05/2018
ms.keywords: GetText, GetText method [Windows Management Instrumentation], GetText method [Windows Management Instrumentation],IWbemPathKeyList interface, IWbemPathKeyList interface [Windows Management Instrumentation],GetText method, IWbemPathKeyList.GetText, IWbemPathKeyList::GetText, WBEMPATH_QUOTEDTEXT, WBEMPATH_TEXT, _hmm_iwbempathkeylist_gettext, wmi.iwbempathkeylist_gettext, wmiutils/IWbemPathKeyList::GetText
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
 - IWbemPathKeyList::GetText
 - wmiutils/IWbemPathKeyList::GetText
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
 - IWbemPathKeyList.GetText
---

# IWbemPathKeyList::GetText


## -description

The 
<b>IWbemPathKeyList::GetText</b> method retrieves the key list as text.

## -parameters

### -param lFlags [in]

Flags which control the format of the text. The following list lists the valid flag values.



#### WBEMPATH_QUOTEDTEXT

Places quotes around the string key values.



#### WBEMPATH_TEXT

Not used.

### -param puBuffLength [in, out]

Caller sets this to the number of characters that the buffer can hold. Upon success, this is set to the number of characters copied into the buffer, including the <b>NULL</b> terminator.

### -param pszText [in, out]

Buffer into which the text is copied.

## -returns

This method returns an <b>HRESULT</b> indicating the status of the method call.

## -remarks

This method can be used to determine how big a buffer is needed by passing in a <b>NULL</b> pointer for the buffer and setting its size parameter to 0 (zero). Upon return, the buffer's size parameter indicates how large of a buffer is needed for the string and its <b>NULL</b> terminator.

## -see-also

<a href="/windows/desktop/api/wmiutils/nn-wmiutils-iwbempath">IWbemPath</a>



<a href="/windows/desktop/api/wmiutils/nn-wmiutils-iwbempathkeylist">IWbemPathKeyList</a>