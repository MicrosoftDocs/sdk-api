---
UID: NF:msaatext.ITfMSAAControl.SystemDisableMSAA
title: ITfMSAAControl::SystemDisableMSAA (msaatext.h)
description: ITfMSAAControl::SystemDisableMSAA method
helpviewer_keywords: ["ITfMSAAControl interface [Text Services Framework]","SystemDisableMSAA method","ITfMSAAControl.SystemDisableMSAA","ITfMSAAControl::SystemDisableMSAA","SystemDisableMSAA","SystemDisableMSAA method [Text Services Framework]","SystemDisableMSAA method [Text Services Framework]","ITfMSAAControl interface","msaatext/ITfMSAAControl::SystemDisableMSAA","tsf.itfmsaacontrol_systemdisablemsaa"]
old-location: tsf\itfmsaacontrol_systemdisablemsaa.htm
tech.root: TSF
ms.assetid: 344cabbb-286e-415d-980f-349fb637a78d
ms.date: 12/05/2018
ms.keywords: ITfMSAAControl interface [Text Services Framework],SystemDisableMSAA method, ITfMSAAControl.SystemDisableMSAA, ITfMSAAControl::SystemDisableMSAA, SystemDisableMSAA, SystemDisableMSAA method [Text Services Framework], SystemDisableMSAA method [Text Services Framework],ITfMSAAControl interface, msaatext/ITfMSAAControl::SystemDisableMSAA, tsf.itfmsaacontrol_systemdisablemsaa
req.header: msaatext.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: MSAAText.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msctf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfMSAAControl::SystemDisableMSAA
 - msaatext/ITfMSAAControl::SystemDisableMSAA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITfMSAAControl.SystemDisableMSAA
---

# ITfMSAAControl::SystemDisableMSAA


## -description

Used by MSAA to halt TSF support of an MSAA client.



## -returns

This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/msaatext/nn-msaatext-itfmsaacontrol">ITfMSAAControl</a>



<a href="/previous-versions/ms971350(v=msdn.10)">Microsoft Active Accessibility</a>
