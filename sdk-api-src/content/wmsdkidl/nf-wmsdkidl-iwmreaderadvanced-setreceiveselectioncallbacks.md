---
UID: NF:wmsdkidl.IWMReaderAdvanced.SetReceiveSelectionCallbacks
title: IWMReaderAdvanced::SetReceiveSelectionCallbacks (wmsdkidl.h)
description: The SetReceiveSelectionCallbacks method specifies whether stream selection notifications must be sent to IWMReaderCallbackAdvanced::OnStreamSelection.helpviewer_keywords: ["IWMReaderAdvanced interface [windows Media Format]","SetReceiveSelectionCallbacks method","IWMReaderAdvanced.SetReceiveSelectionCallbacks","IWMReaderAdvanced::SetReceiveSelectionCallbacks","IWMReaderAdvancedSetReceiveSelectionCallbacks","SetReceiveSelectionCallbacks","SetReceiveSelectionCallbacks method [windows Media Format]","SetReceiveSelectionCallbacks method [windows Media Format]","IWMReaderAdvanced interface","wmformat.iwmreaderadvanced_setreceiveselectioncallbacks","wmsdkidl/IWMReaderAdvanced::SetReceiveSelectionCallbacks"]
old-location: wmformat\iwmreaderadvanced_setreceiveselectioncallbacks.htm
tech.root: wmformat
ms.assetid: 8cb0bd59-2a46-4cdc-9a88-ee6a8f170f3c
ms.date: 12/05/2018
ms.keywords: IWMReaderAdvanced interface [windows Media Format],SetReceiveSelectionCallbacks method, IWMReaderAdvanced.SetReceiveSelectionCallbacks, IWMReaderAdvanced::SetReceiveSelectionCallbacks, IWMReaderAdvancedSetReceiveSelectionCallbacks, SetReceiveSelectionCallbacks, SetReceiveSelectionCallbacks method [windows Media Format], SetReceiveSelectionCallbacks method [windows Media Format],IWMReaderAdvanced interface, wmformat.iwmreaderadvanced_setreceiveselectioncallbacks, wmsdkidl/IWMReaderAdvanced::SetReceiveSelectionCallbacks
f1_keywords:
- wmsdkidl/IWMReaderAdvanced.SetReceiveSelectionCallbacks
dev_langs:
- c++
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
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMReaderAdvanced::SetReceiveSelectionCallbacks


## -description



The <b>SetReceiveSelectionCallbacks</b> method specifies whether stream selection notifications must be sent to <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-onstreamselection">IWMReaderCallbackAdvanced::OnStreamSelection</a>.




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




<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced">IWMReaderAdvanced Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getreceiveselectioncallbacks">IWMReaderAdvanced::GetReceiveSelectionCallbacks</a>
 

 

