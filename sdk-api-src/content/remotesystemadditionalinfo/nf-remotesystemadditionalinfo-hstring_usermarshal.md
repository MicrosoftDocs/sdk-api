---
UID: NF:remotesystemadditionalinfo.HSTRING_UserMarshal
title: HSTRING_UserMarshal function
author: windows-driver-content
description: Marshals an HSTRING object into the RPC buffer.
old-location: winrt\hstring_usermarshal.htm
old-project: WinRT
ms.assetid: 986942D6-A1CD-4BED-9AD3-82FB4892E28E
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: HSTRING_UserMarshal, HSTRING_UserMarshal function [Windows Runtime], remotesystemadditionalinfo/HSTRING_UserMarshal, winrt.hstring_usermarshal
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: remotesystemadditionalinfo.h
req.include-header: Winstring.h, Inspectable.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: EVENT_RECORD, *PEVENT_RECORD
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	ComBase.dll
-	API-MS-Win-Core-WinRT-String-l1-1-0.dll
-	API-MS-Win-Core-WinRT-String-L1-1-1.dll
api_name:
-	HSTRING_UserMarshal
product: Windows
targetos: Windows
req.lib: RuntimeObject.lib
req.dll: ComBase.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# HSTRING_UserMarshal function


## -description


Marshals an <a href="https://msdn.microsoft.com/763ACE57-EFDD-482E-851E-668D7756C5DF">HSTRING</a> object into the RPC buffer.


## -parameters




### -param

TBD




#### - pBuffer [in, out]

The current buffer. This pointer may or may not be aligned on entry.


#### - pFlags [in]

The data used by RPC.


#### - ppidl [in]

The string.


## -returns



The value obtained from the returned <b>HRESULT</b> value is <b>S_OK</b>.




## -see-also




<a href="https://msdn.microsoft.com/763ACE57-EFDD-482E-851E-668D7756C5DF">HSTRING</a>
 

 

