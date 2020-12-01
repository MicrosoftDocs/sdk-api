---
UID: NF:imepad.IImePadApplet.Notify
title: IImePadApplet::Notify (imepad.h)
description: Called from IImePad to pass information with a notify code.
helpviewer_keywords: ["IImePadApplet interface [Internationalization for Windows Applications]","Notify method","IImePadApplet.Notify","IImePadApplet::Notify","Notify","Notify method [Internationalization for Windows Applications]","Notify method [Internationalization for Windows Applications]","IImePadApplet interface","imepad/IImePadApplet::Notify","intl.iimepadapplet_notify"]
old-location: intl\iimepadapplet_notify.htm
tech.root: Intl
ms.assetid: 5C370DC8-D308-4339-81F3-FEE88359A52F
ms.date: 12/05/2018
ms.keywords: IImePadApplet interface [Internationalization for Windows Applications],Notify method, IImePadApplet.Notify, IImePadApplet::Notify, Notify, Notify method [Internationalization for Windows Applications], Notify method [Internationalization for Windows Applications],IImePadApplet interface, imepad/IImePadApplet::Notify, intl.iimepadapplet_notify
req.header: imepad.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IImePadApplet::Notify
 - imepad/IImePadApplet::Notify
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Imepad.h
api_name:
 - IImePadApplet.Notify
---

# IImePadApplet::Notify


## -description

Called from <a href="/windows/desktop/api/imepad/nn-imepad-iimepad">IImePad</a> to pass information with a notify code

## -parameters

### -param lpImePad [in]

Pointer of IUnknown interface. To get the <a href="/windows/desktop/api/imepad/nn-imepad-iimepad">IImePad</a> interface pointer, use <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a>.

### -param notify [in]

The <a href="/windows/desktop/api/imepad/nn-imepad-iimepadapplet">IImePadApplet</a> notify code. See Remarks for the possible codes.

### -param wParam [in, out]

Additional information specific to <i>notify</i>.

### -param lParam [in, out]

Additional information specific to <i>notify</i>.

## -returns

<b>S_OK</b> if successful, otherwise <b>E_FAIL</b>.

## -remarks

<h3><a id="Possible_notify_codes__IMEPN___values_"></a><a id="possible_notify_codes__imepn___values_"></a><a id="POSSIBLE_NOTIFY_CODES__IMEPN___VALUES_"></a>Possible notify codes (<b>IMEPN_*</b> values)</h3>

<table>
<tr>
<th>Code</th>
<th>Description</th>
</tr>
<tr>
<td><b>IMEPN_ACTIVATE</b></td>
<td>The applet is activated.</td>
</tr>
<tr>
<td><b>IMEPN_INACTIVATE</b></td>
<td>The applet is inactivate.</td>
</tr>
<tr>
<td><b>IMEPN_SHOW</b></td>
<td>IMEPad and the applet are shown.</td>
</tr>
<tr>
<td><b>IMEPN_HIDE</b></td>
<td>IMEPad and the applet are hidden.</td>
</tr>
<tr>
<td><b>IMEPN_SIZECHANGING</b></td>
<td>The applet size is changing.</td>
</tr>
<tr>
<td><b>IMEPN_SIZECHANGED</b></td>
<td>The applet size has changed.</td>
</tr>
<tr>
<td><b>IMEPN_CONFIG</b></td>
<td>The applet setting is selected in IMEPad menu.</td>
</tr>
<tr>
<td><b>IMEPN_HELP</b></td>
<td>The applet help is selected in IMEPad menu.</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/imepad/nn-imepad-iimepadapplet">IImePadApplet</a>