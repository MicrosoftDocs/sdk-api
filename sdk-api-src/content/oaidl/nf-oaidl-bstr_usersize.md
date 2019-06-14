---
UID: NF:oaidl.BSTR_UserSize
title: BSTR_UserSize function (oaidl.h)
author: windows-sdk-content
description: Calculates the wire size of the BSTR object, and gets its handle and data.
old-location: automat\bstr_usersize.htm
tech.root: automat
ms.assetid: 16c349b4-21e1-45bb-8b24-d299adb36e14
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: BSTR_UserSize, BSTR_UserSize function [Automation], _oa96_BSTR_UserSize, automat.bstr_usersize, oaidl/BSTR_UserSize
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
 - BSTR_UserSize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# BSTR_UserSize function


## -description


Calculates the wire size of the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/automat/bstr">BSTR</a> object, and gets its handle and data.


## -parameters




### -param arg1 [in]

The data used by RPC.


### -param arg2 [in]

The current buffer offset where the object will be marshaled. The method has to account for any padding needed for the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/automat/bstr">BSTR</a> object to be properly aligned when it will be marshaled to the buffer.


### -param arg3 [in]

The object.


## -returns



The value obtained from the returned <b>HRESULT</b> value is <b>S_OK</b>.



