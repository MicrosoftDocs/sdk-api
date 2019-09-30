---
UID: NF:oaidl.BSTR_UserMarshal
title: BSTR_UserMarshal function (oaidl.h)
author: windows-sdk-content
description: Marshals a BSTR object into the RPC buffer.
old-location: automat\bstr_usermarshal.htm
tech.root: automat
ms.assetid: 98825155-1dd3-47c0-928d-484d5bc70927
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: BSTR_UserMarshal, BSTR_UserMarshal function [Automation], _oa96_BSTR_UserMarshal, automat.bstr_usermarshal, oaidl/BSTR_UserMarshal
ms.topic: function
f1_keywords: 
 - "oaidl/BSTR_UserMarshal"
req.header: oaidl.h
req.include-header: 
req.target-type: Windows
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
 - BSTR_UserMarshal
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# BSTR_UserMarshal function


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



