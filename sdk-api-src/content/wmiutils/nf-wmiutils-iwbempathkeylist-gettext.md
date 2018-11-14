---
UID: NF:wmiutils.IWbemPathKeyList.GetText
title: IWbemPathKeyList::GetText
author: windows-sdk-content
description: The IWbemPathKeyList::GetText method retrieves the key list as text.
old-location: wmi\iwbempathkeylist_gettext.htm
tech.root: WmiSdk
ms.assetid: 01c69709-be6e-4a58-849d-76f9d4e3c196
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: GetText, GetText method [Windows Management Instrumentation], GetText method [Windows Management Instrumentation],IWbemPathKeyList interface, IWbemPathKeyList interface [Windows Management Instrumentation],GetText method, IWbemPathKeyList.GetText, IWbemPathKeyList::GetText, WBEMPATH_QUOTEDTEXT, WBEMPATH_TEXT, _hmm_iwbempathkeylist_gettext, wmi.iwbempathkeylist_gettext, wmiutils/IWbemPathKeyList::GetText
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: Wbemuuid.lib
req.dll: Wmiutils.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmiutils.dll
api_name:
 - IWbemPathKeyList.GetText
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- wmiutils.h
: 
- IWbemPathKeyList.GetText
: 
---

# IWbemPathKeyList::GetText


## -description


The 
<b>IWbemPathKeyList::GetText</b> method retrieves the key list as text.


## -parameters




### -param lFlags [in]

Flags which control the format of the text. The following list lists the valid flag values.



#### WBEMPATH_QUOTEDTEXT

Places quotes around the string key values.



#### WBEMPATH_TEXT

Not used.


### -param puBuffLength [in, out]

Caller sets this to the number of characters that the buffer can hold. Upon success, this is set to the number of characters copied into the buffer, including the <b>NULL</b> terminator.


### -param pszText [in, out]

Buffer into which the text is copied.


## -returns



This method returns an <b>HRESULT</b> indicating the status of the method call.




## -remarks



This method can be used to determine how big a buffer is needed by passing in a <b>NULL</b> pointer for the buffer and setting its size parameter to 0 (zero). Upon return, the buffer's size parameter indicates how large of a buffer is needed for the string and its <b>NULL</b> terminator.




## -see-also




<a href="https://msdn.microsoft.com/71b2597b-d82a-439d-b0b7-af76aefea6a2">IWbemPath</a>



<a href="https://msdn.microsoft.com/5b188426-9d7f-4e87-9eed-ce80e5d93c30">IWbemPathKeyList</a>
 

 

