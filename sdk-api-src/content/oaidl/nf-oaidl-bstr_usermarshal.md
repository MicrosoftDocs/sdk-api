---
UID: NF:oaidl.BSTR_UserMarshal
title: BSTR_UserMarshal function
author: windows-sdk-content
description: Marshals a BSTR object into the RPC buffer.
old-location: automat\bstr_usermarshal.htm
tech.root: automat
ms.assetid: 98825155-1dd3-47c0-928d-484d5bc70927
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: BSTR_UserMarshal, BSTR_UserMarshal function [Automation], _oa96_BSTR_UserMarshal, automat.bstr_usermarshal, oaidl/BSTR_UserMarshal
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# BSTR_UserMarshal function


## -description


Marshals a <a href="https://msdn.microsoft.com/1b2d7d2c-47af-4389-a6b6-b01b7e915228">BSTR</a> object into the RPC buffer.


## -parameters




### -param arg1

TBD


### -param arg2

TBD


### -param arg3

TBD




#### - [in]

The data used by RPC.


#### - pBstr [in]

The object.


#### - pBuffer [in, out]

The current buffer. This pointer may or may not be aligned on entry.


## -returns



The value obtained from the returned <b>HRESULT</b> value is <b>S_OK</b>.



