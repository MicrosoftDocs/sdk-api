---
UID: NF:wmiutils.IWbemPath.SetText
title: IWbemPath::SetText
author: windows-sdk-content
description: The IWbemPath::SetText method parses a path so that information on the path can be returned by the path parser.
old-location: wmi\iwbempath_settext.htm
old-project: WmiSdk
ms.assetid: a3ff2aa9-ffa8-4048-ac07-4b815b620d1f
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: IWbemPath interface [Windows Management Instrumentation],SetText method, IWbemPath.SetText, IWbemPath::SetText, SetText, SetText method [Windows Management Instrumentation], SetText method [Windows Management Instrumentation],IWbemPath interface, WBEMPATH_CREATE_ACCEPT_ABSOLUTE, WBEMPATH_CREATE_ACCEPT_ALL, WBEMPATH_CREATE_ACCEPT_RELATIVE, WBEMPATH_TREAT_SINGLE_IDENT_AS_NS, _hmm_iwbempath_settext, wmi.iwbempath_settext, wmiutils/IWbemPath::SetText
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wmiutils.dll
api_name:
-	IWbemPath.SetText
product: Windows
targetos: Windows
req.lib: Wbemuuid.lib
req.dll: Wmiutils.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWbemPath::SetText


## -description


The 
<b>IWbemPath::SetText</b> method parses a path so that information on the path can be returned by the path parser. Typically, this is the first method called by users of the interface. The only case in which this is not the first method called is when the calling code is constructing the path by specifying each piece separately.


## -parameters




### -param uMode [in]

Flag specifying the type of paths accepted.



#### WBEMPATH_CREATE_ACCEPT_RELATIVE

Allow paths without server names.



#### WBEMPATH_CREATE_ACCEPT_ABSOLUTE

Reserved for future use.



#### WBEMPATH_CREATE_ACCEPT_ALL

Allow setting an empty path (which additionally clears out the object), Also allows paths which have just the server names, or paths which don't have server names.



#### WBEMPATH_TREAT_SINGLE_IDENT_AS_NS

A simple path, such as "XYZ" is interpreted as a namespace.


### -param pszPath [in]

Path to be parsed.


## -returns



This method returns an <b>HRESULT</b> indicating the status of the method call.




## -see-also




<a href="https://msdn.microsoft.com/71b2597b-d82a-439d-b0b7-af76aefea6a2">IWbemPath</a>
 

 

