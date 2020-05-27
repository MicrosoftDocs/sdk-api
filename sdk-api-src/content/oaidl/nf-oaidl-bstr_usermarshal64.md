---
UID: NF:oaidl.BSTR_UserMarshal64
title: BSTR_UserMarshal64 function (oaidl.h)
description: Marshals a BSTR object into the RPC buffer.
helpviewer_keywords: ["BSTR_UserMarshal64","BSTR_UserMarshal64 function [Automation]","automat.bstr_usermarshal64","oaidl/BSTR_UserMarshal64"]
old-location: automat\bstr_usermarshal64.htm
tech.root: automat
ms.assetid: f61b9e6b-14f1-4171-97c7-169547286626
ms.date: 12/05/2018
ms.keywords: BSTR_UserMarshal64, BSTR_UserMarshal64 function [Automation], automat.bstr_usermarshal64, oaidl/BSTR_UserMarshal64
f1_keywords:
- oaidl/BSTR_UserMarshal64
dev_langs:
- c++
req.header: oaidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: OleAut32.lib
req.dll: OleAut32.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- OleAut32.dll
api_name:
- BSTR_UserMarshal64
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# BSTR_UserMarshal64 function


## -description


Marshals a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/automat/bstr">BSTR</a> object into the RPC buffer.


## -parameters




### -param arg1 [in]

The data used by RPC.


### -param arg2 [in, out]

The current buffer. This pointer may or may not be aligned on entry.


### -param arg3 [in]

The object.


## -returns



The value obtained from the returned <b>HRESULT</b> value is <b>S_OK</b>.



