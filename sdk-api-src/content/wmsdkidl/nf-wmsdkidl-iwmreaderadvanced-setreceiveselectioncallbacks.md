---
UID: NF:wmsdkidl.IWMReaderAdvanced.SetReceiveSelectionCallbacks
title: IWMReaderAdvanced::SetReceiveSelectionCallbacks
author: windows-sdk-content
description: The SetReceiveSelectionCallbacks method specifies whether stream selection notifications must be sent to IWMReaderCallbackAdvanced::OnStreamSelection.
old-location: wmformat\iwmreaderadvanced_setreceiveselectioncallbacks.htm
old-project: wmformat
ms.assetid: 8cb0bd59-2a46-4cdc-9a88-ee6a8f170f3c
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: IWMReaderAdvanced interface [windows Media Format],SetReceiveSelectionCallbacks method, IWMReaderAdvanced.SetReceiveSelectionCallbacks, IWMReaderAdvanced::SetReceiveSelectionCallbacks, IWMReaderAdvancedSetReceiveSelectionCallbacks, SetReceiveSelectionCallbacks, SetReceiveSelectionCallbacks method [windows Media Format], SetReceiveSelectionCallbacks method [windows Media Format],IWMReaderAdvanced interface, wmformat.iwmreaderadvanced_setreceiveselectioncallbacks, wmsdkidl/IWMReaderAdvanced::SetReceiveSelectionCallbacks
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
tech.root: 
req.typenames: WM_AETYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmvcore.lib
 - Wmvcore.dll
 - WMStubDRM.lib
 - WMStubDRM.dll
api_name:
 - IWMReaderAdvanced.SetReceiveSelectionCallbacks
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMReaderAdvanced::SetReceiveSelectionCallbacks


## -description



The <b>SetReceiveSelectionCallbacks</b> method specifies whether stream selection notifications must be sent to <a href="https://msdn.microsoft.com/d0d699b3-e2f3-427c-9159-e2ed875887ca">IWMReaderCallbackAdvanced::OnStreamSelection</a>.




## -parameters




### -param fGetCallbacks [in]

Boolean value that is True if stream selections must generate callbacks.


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
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
No callback interface has been specified.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/a7a20f87-6f21-4fe8-8889-1b6689daf833">IWMReaderAdvanced Interface</a>



<a href="https://msdn.microsoft.com/7923564d-23d5-4163-9316-347c466c7dc0">IWMReaderAdvanced::GetReceiveSelectionCallbacks</a>
 

 

