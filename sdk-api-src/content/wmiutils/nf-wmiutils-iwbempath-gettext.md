---
UID: NF:wmiutils.IWbemPath.GetText
title: IWbemPath::GetText
author: windows-sdk-content
description: The IWbemPath::GetText method returns a textual representation of a path that has previously been placed into a parser object.
old-location: wmi\iwbempath_gettext.htm
old-project: WmiSdk
ms.assetid: 427ff33a-3b46-481e-bf46-57b13d19332e
ms.author: windowssdkdev
ms.date: 08/28/2018
ms.keywords: GetText, GetText method [Windows Management Instrumentation], GetText method [Windows Management Instrumentation],IWbemPath interface, IWbemPath interface [Windows Management Instrumentation],GetText method, IWbemPath.GetText, IWbemPath::GetText, WBEMPATH_COMPRESSED, WBEMPATH_GET_NAMESPACE_ONLY, WBEMPATH_GET_ORIGINAL, WBEMPATH_GET_RELATIVE_ONLY, WBEMPATH_GET_SERVER_AND_NAMESPACE_ONLY, WBEMPATH_GET_SERVER_TOO, _hmm_iwbempath_gettext, wmi.iwbempath_gettext, wmiutils/IWbemPath::GetText
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wmiutils.h
req.include-header: 
req.redist: 
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
 - IWbemPath.GetText
product: Windows
targetos: Windows
req.lib: Wbemuuid.lib
req.dll: Wmiutils.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWbemPath::GetText


## -description


The 
<b>IWbemPath::GetText</b> method returns a textual representation of a path that has previously been placed into a parser object.


## -parameters




### -param lFlags [in]

Flag which controls how the text is returned.



#### WBEMPATH_COMPRESSED

Obsolete. Do not use.



#### WBEMPATH_GET_RELATIVE_ONLY

Returns the relative path, skips server and namespaces.



#### WBEMPATH_GET_SERVER_TOO

Returns the entire path, including server and namespace.



#### WBEMPATH_GET_SERVER_AND_NAMESPACE_ONLY

Returns only the server and namespace portion of the path. Ignores the class or key portion.



#### WBEMPATH_GET_NAMESPACE_ONLY

Returns only the namespace portion of the path.



#### WBEMPATH_GET_ORIGINAL

Returns whatever was passed in using 
<a href="https://msdn.microsoft.com/a3ff2aa9-ffa8-4048-ac07-4b815b620d1f">SetText</a> method.


### -param puBuffLength [in, out]

Caller sets this to the size of <i>pszText</i>. If the method is successful, it sets <i>puBufferLength</i> to the number of wide characters used, including the terminating null character.


### -param pszText [in, out]

Textual representation of the path.


## -returns



This method returns the following values.




## -see-also




<a href="https://msdn.microsoft.com/71b2597b-d82a-439d-b0b7-af76aefea6a2">IWbemPath</a>
 

 

