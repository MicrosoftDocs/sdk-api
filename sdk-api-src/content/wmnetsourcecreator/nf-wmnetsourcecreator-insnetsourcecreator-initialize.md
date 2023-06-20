---
UID: NF:wmnetsourcecreator.INSNetSourceCreator.Initialize
title: INSNetSourceCreator::Initialize (wmnetsourcecreator.h)
description: The Initialize method prepares the network source creator for operations. You must call this method before calling any of the other methods in the INSNetSourceCreator interface.
helpviewer_keywords: ["INSNetSourceCreator interface [windows Media Format]","Initialize method","INSNetSourceCreator.Initialize","INSNetSourceCreator::Initialize","INSNetSourceCreatorInitialize","Initialize","Initialize method [windows Media Format]","Initialize method [windows Media Format]","INSNetSourceCreator interface","wmformat.insnetsourcecreator_initialize","wmnetsourcecreator/INSNetSourceCreator::Initialize"]
old-location: wmformat\insnetsourcecreator_initialize.htm
tech.root: wmformat
ms.assetid: 53c1a15e-3ced-44e5-b512-b381ae11aa65
ms.date: 4/26/2023
ms.keywords: INSNetSourceCreator interface [windows Media Format],Initialize method, INSNetSourceCreator.Initialize, INSNetSourceCreator::Initialize, INSNetSourceCreatorInitialize, Initialize, Initialize method [windows Media Format], Initialize method [windows Media Format],INSNetSourceCreator interface, wmformat.insnetsourcecreator_initialize, wmnetsourcecreator/INSNetSourceCreator::Initialize
req.header: wmnetsourcecreator.h
req.include-header: 
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - INSNetSourceCreator::Initialize
 - wmnetsourcecreator/INSNetSourceCreator::Initialize
dev_langs:
 - c++
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
 - INSNetSourceCreator.Initialize
---

# INSNetSourceCreator::Initialize


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>Initialize</b> method prepares the network source creator for operations. You must call this method before calling any of the other methods in the <b>INSNetSourceCreator</b> interface.



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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The method could not allocate memory for an internal resource.

</td>
</tr>
</table>

## -remarks

When you are finished using the network source creator, you must call the <a href="/windows/desktop/api/wmnetsourcecreator/nf-wmnetsourcecreator-insnetsourcecreator-shutdown">Shutdown</a> method to ensure that all resources are released properly.

## -see-also

<a href="/windows/desktop/api/wmnetsourcecreator/nn-wmnetsourcecreator-insnetsourcecreator">INSNetSourceCreator Interface</a>



<a href="/windows/desktop/api/wmnetsourcecreator/nf-wmnetsourcecreator-insnetsourcecreator-shutdown">INSNetSourceCreator::Shutdown</a>
