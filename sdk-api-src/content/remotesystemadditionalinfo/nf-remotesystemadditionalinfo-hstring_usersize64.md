---
UID: NF:remotesystemadditionalinfo.HSTRING_UserSize64
title: HSTRING_UserSize64 function
author: windows-sdk-content
description: Calculates the wire size of the HSTRING object, and gets its handle and data.
old-location: winrt\hstring_usersize64.htm
old-project: WinRT
ms.assetid: 38ACC82C-959C-4E15-ABEF-0B92EE712E87
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: HSTRING_UserSize64, HSTRING_UserSize64 function [Windows Runtime], remotesystemadditionalinfo/HSTRING_UserSize64, winrt.hstring_usersize64
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: remotesystemadditionalinfo.h
req.include-header: Winstring.h, Inspectable.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
req.typenames: EVENT_RECORD, *PEVENT_RECORD
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ComBase.dll
 - API-MS-Win-Core-WinRT-String-l1-1-0.dll
 - API-MS-Win-Core-WinRT-String-L1-1-1.dll
api_name:
 - HSTRING_UserSize64
product: Windows
targetos: Windows
req.lib: RuntimeObject.lib
req.dll: ComBase.dll
req.irql: 
req.product: ADAM
---

# HSTRING_UserSize64 function


## -description


Calculates the wire size of the <a href="https://msdn.microsoft.com/763ACE57-EFDD-482E-851E-668D7756C5DF">HSTRING</a> object, and gets its handle and data.


## -parameters




### -param

TBD




#### - StartingSize [in]

The current buffer offset where the object will be marshaled. The method has to account for any padding needed for the <a href="https://msdn.microsoft.com/763ACE57-EFDD-482E-851E-668D7756C5DF">HSTRING</a> object to be properly aligned when it will be marshaled to the buffer.


#### - pFlags [in]

The data used by RPC.


#### - ppidl [in]

The string.


## -returns



The value obtained from the returned <b>HRESULT</b> value is <b>S_OK</b>.




## -see-also




<a href="https://msdn.microsoft.com/763ACE57-EFDD-482E-851E-668D7756C5DF">HSTRING</a>
 

 

