---
UID: NF:wmsdkidl.IWMReaderAdvanced.GetUserProvidedClock
title: IWMReaderAdvanced::GetUserProvidedClock
author: windows-sdk-content
description: The GetUserProvidedClock method ascertains whether a user-provided clock has been specified.
old-location: wmformat\iwmreaderadvanced_getuserprovidedclock.htm
old-project: wmformat
ms.assetid: 54eb30ae-4b84-489c-a5e5-e73dee2c5056
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: GetUserProvidedClock, GetUserProvidedClock method [windows Media Format], GetUserProvidedClock method [windows Media Format],IWMReaderAdvanced interface, IWMReaderAdvanced interface [windows Media Format],GetUserProvidedClock method, IWMReaderAdvanced.GetUserProvidedClock, IWMReaderAdvanced::GetUserProvidedClock, IWMReaderAdvancedGetUserProvidedClock, wmformat.iwmreaderadvanced_getuserprovidedclock, wmsdkidl/IWMReaderAdvanced::GetUserProvidedClock
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 7 SDK, or later versions of the SDK
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WM_AETYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wmvcore.lib
-	Wmvcore.dll
-	WMStubDRM.lib
-	WMStubDRM.dll
api_name:
-	IWMReaderAdvanced.GetUserProvidedClock
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMReaderAdvanced::GetUserProvidedClock


## -description



The <b>GetUserProvidedClock</b> method ascertains whether a user-provided clock has been specified.




## -parameters




### -param pfUserClock [out]

Pointer to a Boolean value that is set to True if a user-provided clock has been specified.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pfUserClock</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/a7a20f87-6f21-4fe8-8889-1b6689daf833">IWMReaderAdvanced Interface</a>



<a href="https://msdn.microsoft.com/1f29beea-1da4-41e0-a68d-93af3b1f55ed">IWMReaderAdvanced::SetUserProvidedClock</a>
 

 

