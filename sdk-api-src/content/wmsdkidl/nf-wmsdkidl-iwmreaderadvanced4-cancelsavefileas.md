---
UID: NF:wmsdkidl.IWMReaderAdvanced4.CancelSaveFileAs
title: IWMReaderAdvanced4::CancelSaveFileAs
author: windows-sdk-content
description: The CancelSaveFileAs method cancels a file save resulting from a call to IWMReaderAdvanced2::SaveFileAs.
old-location: wmformat\iwmreaderadvanced4_cancelsavefileas.htm
old-project: wmformat
ms.assetid: fcf43e86-daa3-4944-b687-b8c9afab7336
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: CancelSaveFileAs, CancelSaveFileAs method [windows Media Format], CancelSaveFileAs method [windows Media Format],IWMReaderAdvanced4 interface, IWMReaderAdvanced4 interface [windows Media Format],CancelSaveFileAs method, IWMReaderAdvanced4.CancelSaveFileAs, IWMReaderAdvanced4::CancelSaveFileAs, IWMReaderAdvanced4CancelSaveFileAs, wmformat.iwmreaderadvanced4_cancelsavefileas, wmsdkidl/IWMReaderAdvanced4::CancelSaveFileAs
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
 - IWMReaderAdvanced4.CancelSaveFileAs
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMReaderAdvanced4::CancelSaveFileAs


## -description



The <b>CancelSaveFileAs</b> method cancels a file save resulting from a call to <a href="https://msdn.microsoft.com/97bdac1f-8830-45c0-9229-322ad72b3954">IWMReaderAdvanced2::SaveFileAs</a>.




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




<a href="https://msdn.microsoft.com/56695c57-f6c5-4c57-b3d4-73d169b379fa">IWMReaderAdvanced4 Interface</a>
 

 

