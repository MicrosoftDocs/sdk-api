---
UID: NF:wmiutils.IWbemPath.GetScopeAsText
title: IWbemPath::GetScopeAsText
author: windows-sdk-content
description: Retrieves a scope in text format based on an index.
old-location: wmi\iwbempath_getscopeastext.htm
old-project: WmiSdk
ms.assetid: f43d2215-7950-421b-b660-ebe89f24407e
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: GetScopeAsText, GetScopeAsText method [Windows Management Instrumentation], GetScopeAsText method [Windows Management Instrumentation],IWbemPath interface, IWbemPath interface [Windows Management Instrumentation],GetScopeAsText method, IWbemPath.GetScopeAsText, IWbemPath::GetScopeAsText, _hmm_iwbempath_getscopeastext, wmi.iwbempath_getscopeastext, wmiutils/IWbemPath::GetScopeAsText
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: WMIQ_ASSOCQ_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmiutils.dll
api_name:
 - IWbemPath.GetScopeAsText
product: Windows
targetos: Windows
req.lib: Wbemuuid.lib
req.dll: Wmiutils.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWbemPath::GetScopeAsText


## -description


The 
<b>IWbemPath::GetScopeAsText</b> method retrieves a scope in text format based on an index.


## -parameters




### -param uIndex [in]

Index of the scope.


### -param puTextBufSize [in, out]

Caller sets this to the number of characters that the buffer can hold. After success this is set to the number of characters copied into the buffer including the <b>NULL</b> terminator.


### -param pszText [out]

Buffer where the scope is to be copied.


## -returns



This method returns the following values.




## -remarks



This method can be used to determine how big a buffer is needed for <i>pszText</i>. This is done by passing in a <b>NULL</b> pointer for the buffer, setting <i>puTextBufSize</i> to zero (0), and then making the call. When returned, <i>puTextBufSize</i> indicates how large  a buffer is needed for <i>pszText</i> and its terminating <b>NULL</b> character.




## -see-also




<a href="https://msdn.microsoft.com/71b2597b-d82a-439d-b0b7-af76aefea6a2">IWbemPath</a>
 

 

