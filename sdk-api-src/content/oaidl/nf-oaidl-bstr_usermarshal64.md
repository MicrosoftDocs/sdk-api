---
UID: NF:oaidl.BSTR_UserMarshal64
title: BSTR_UserMarshal64 function
author: windows-sdk-content
description: Marshals a BSTR object into the RPC buffer.
old-location: automat\bstr_usermarshal64.htm
old-project: automat
ms.assetid: f61b9e6b-14f1-4171-97c7-169547286626
ms.author: windowssdkdev
ms.date: 05/04/2018
ms.keywords: BSTR_UserMarshal64, BSTR_UserMarshal64 function [Automation], automat.bstr_usermarshal64, oaidl/BSTR_UserMarshal64
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: oaidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: VARKIND
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	OleAut32.dll
api_name:
-	BSTR_UserMarshal64
product: Windows
targetos: Windows
req.lib: OleAut32.lib
req.dll: OleAut32.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# BSTR_UserMarshal64 function


## -description


Marshals a <a href="https://msdn.microsoft.com/1b2d7d2c-47af-4389-a6b6-b01b7e915228">BSTR</a> object into the RPC buffer.


## -parameters




### -param

TBD




#### - pBstr [in]

The object.


#### - pBuffer [in, out]

The current buffer. This pointer may or may not be aligned on entry.


#### - pFlags [in]

The data used by RPC.


## -returns



The value obtained from the returned <b>HRESULT</b> value is <b>S_OK</b>.



