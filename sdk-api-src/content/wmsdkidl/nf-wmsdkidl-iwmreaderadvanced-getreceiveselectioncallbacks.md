---
UID: NF:wmsdkidl.IWMReaderAdvanced.GetReceiveSelectionCallbacks
title: IWMReaderAdvanced::GetReceiveSelectionCallbacks
author: windows-driver-content
description: The GetReceiveSelectionCallbacks method ascertains whether the option to receive stream selection notifications has been enabled.
old-location: wmformat\iwmreaderadvanced_getreceiveselectioncallbacks.htm
old-project: wmformat
ms.assetid: 7923564d-23d5-4163-9316-347c466c7dc0
ms.author: windowsdriverdev
ms.date: 4/13/2018
ms.keywords: GetReceiveSelectionCallbacks, GetReceiveSelectionCallbacks method [windows Media Format], GetReceiveSelectionCallbacks method [windows Media Format],IWMReaderAdvanced interface, IWMReaderAdvanced interface [windows Media Format],GetReceiveSelectionCallbacks method, IWMReaderAdvanced.GetReceiveSelectionCallbacks, IWMReaderAdvanced::GetReceiveSelectionCallbacks, IWMReaderAdvancedGetReceiveSelectionCallbacks, wmformat.iwmreaderadvanced_getreceiveselectioncallbacks, wmsdkidl/IWMReaderAdvanced::GetReceiveSelectionCallbacks
ms.prod: windows-hardware
ms.technology: windows-devices
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
-	IWMReaderAdvanced.GetReceiveSelectionCallbacks
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMReaderAdvanced::GetReceiveSelectionCallbacks


## -description



The <b>GetReceiveSelectionCallbacks</b> method ascertains whether the option to receive stream selection notifications has been enabled.




## -parameters




### -param pfGetCallbacks [out]

Pointer to a Boolean value that is set to True if stream selection notifications are sent to <a href="https://msdn.microsoft.com/d0d699b3-e2f3-427c-9159-e2ed875887ca">IWMReaderCallbackAdvanced::OnStreamSelection</a>.


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
The <i>pfGetCallbacks</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/a7a20f87-6f21-4fe8-8889-1b6689daf833">IWMReaderAdvanced Interface</a>



<a href="https://msdn.microsoft.com/8cb0bd59-2a46-4cdc-9a88-ee6a8f170f3c">IWMReaderAdvanced::SetReceiveSelectionCallbacks</a>
 

 

