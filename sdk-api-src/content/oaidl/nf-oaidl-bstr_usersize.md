---
UID: NF:oaidl.BSTR_UserSize
title: BSTR_UserSize function
author: windows-sdk-content
description: Calculates the wire size of the BSTR object, and gets its handle and data.
old-location: automat\bstr_usersize.htm
old-project: automat
ms.assetid: 16c349b4-21e1-45bb-8b24-d299adb36e14
ms.author: windowssdkdev
ms.date: 05/07/2018
ms.keywords: BSTR_UserSize, BSTR_UserSize function [Automation], _oa96_BSTR_UserSize, automat.bstr_usersize, oaidl/BSTR_UserSize
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: VARKIND
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
req.lib: OleAut32.lib
req.dll: OleAut32.dll
req.irql: 
req.product: ADAM
---

# BSTR_UserSize function


## -description


Calculates the wire size of the <a href="https://msdn.microsoft.com/1b2d7d2c-47af-4389-a6b6-b01b7e915228">BSTR</a> object, and gets its handle and data.


## -parameters




### -param

TBD




#### - Offset [in]

The current buffer offset where the object will be marshaled. The method has to account for any padding needed for the <a href="https://msdn.microsoft.com/1b2d7d2c-47af-4389-a6b6-b01b7e915228">BSTR</a> object to be properly aligned when it will be marshaled to the buffer.


#### - pBstr [in]

The object.


#### - pFlags [in]

The data used by RPC.


## -returns



The value obtained from the returned <b>HRESULT</b> value is <b>S_OK</b>.



