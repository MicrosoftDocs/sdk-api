---
UID: NF:wmsdkidl.IWMReaderAdvanced4.CancelSaveFileAs
title: IWMReaderAdvanced4::CancelSaveFileAs (wmsdkidl.h)
description: The CancelSaveFileAs method cancels a file save resulting from a call to IWMReaderAdvanced2::SaveFileAs.helpviewer_keywords: ["CancelSaveFileAs","CancelSaveFileAs method [windows Media Format]","CancelSaveFileAs method [windows Media Format]","IWMReaderAdvanced4 interface","IWMReaderAdvanced4 interface [windows Media Format]","CancelSaveFileAs method","IWMReaderAdvanced4.CancelSaveFileAs","IWMReaderAdvanced4::CancelSaveFileAs","IWMReaderAdvanced4CancelSaveFileAs","wmformat.iwmreaderadvanced4_cancelsavefileas","wmsdkidl/IWMReaderAdvanced4::CancelSaveFileAs"]
old-location: wmformat\iwmreaderadvanced4_cancelsavefileas.htm
tech.root: wmformat
ms.assetid: fcf43e86-daa3-4944-b687-b8c9afab7336
ms.date: 12/05/2018
ms.keywords: CancelSaveFileAs, CancelSaveFileAs method [windows Media Format], CancelSaveFileAs method [windows Media Format],IWMReaderAdvanced4 interface, IWMReaderAdvanced4 interface [windows Media Format],CancelSaveFileAs method, IWMReaderAdvanced4.CancelSaveFileAs, IWMReaderAdvanced4::CancelSaveFileAs, IWMReaderAdvanced4CancelSaveFileAs, wmformat.iwmreaderadvanced4_cancelsavefileas, wmsdkidl/IWMReaderAdvanced4::CancelSaveFileAs
f1_keywords:
- wmsdkidl/IWMReaderAdvanced4.CancelSaveFileAs
dev_langs:
- c++
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 9 Series SDK, or later versions of the SDK
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
- IWMReaderAdvanced4.CancelSaveFileAs
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMReaderAdvanced4::CancelSaveFileAs


## -description



The <b>CancelSaveFileAs</b> method cancels a file save resulting from a call to <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-savefileas">IWMReaderAdvanced2::SaveFileAs</a>.




## -parameters






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
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4">IWMReaderAdvanced4 Interface</a>
 

 

