---
UID: NN:imepad.IImePadApplet
title: IImePadApplet (imepad.h)

description: The IImePadApplet interface inputs strings into apps through the IImePad interface.
old-location: intl\iimepadapplet.htm
tech.root: Intl
ms.assetid: F3BC7176-9659-47B6-AFCA-049807394961

ms.date: 12/05/2018
ms.keywords: IImePadApplet, IImePadApplet interface [Internationalization for Windows Applications], IImePadApplet interface [Internationalization for Windows Applications],described, imepad/IImePadApplet, intl.iimepadapplet
ms.topic: interface
f1_keywords: 
 - "imepad/IImePadApplet"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Imepad.h
api_name:
 - IImePadApplet
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IImePadApplet interface


## -description


The <b>IImePadApplet</b> interface inputs strings into apps through the <a href="https://docs.microsoft.com/windows/desktop/api/imepad/nn-imepad-iimepad">IImePad</a> interface.

<b>IImePadApplet</b> should be implemented as a DLL inproc server. The developer can implement multiple <b>IImePadApplet</b> interfaces in one DLL.  To specify and emulate the <b>IImePadApplet</b> interface in the applet DLL, the applet must also provide the <a href="https://docs.microsoft.com/windows/desktop/api/imepad/nn-imepad-iimespecifyapplets">IImeSpecifyApplets</a> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IImePadApplet</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IImePadApplet</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IImePadApplet</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imepad/nf-imepad-iimepadapplet-createui">CreateUI</a>
</td>
<td align="left" width="63%">
Called from <a href="https://docs.microsoft.com/windows/desktop/api/imepad/nn-imepad-iimepad">IImePad</a> to get the applet's window handle, style, and size.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh851787(v=vs.85)">GetAppletCfg</a>
</td>
<td align="left" width="63%">
Called from <a href="https://docs.microsoft.com/windows/desktop/api/imepad/nn-imepad-iimepad">IImePad</a> to get <b>IImePadApplet</b>'s configuration data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imepad/nf-imepad-iimepadapplet-initialize">Initialize</a>
</td>
<td align="left" width="63%">
Called from <a href="https://docs.microsoft.com/windows/desktop/api/imepad/nn-imepad-iimepad">IImePad</a> interface to initialize <b>IImePadApplet</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imepad/nf-imepad-iimepadapplet-notify">Notify</a>
</td>
<td align="left" width="63%">
Called from <a href="https://docs.microsoft.com/windows/desktop/api/imepad/nn-imepad-iimepad">IImePad</a> to pass information with a notify code

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imepad/nf-imepad-iimepadapplet-terminate">Terminate</a>
</td>
<td align="left" width="63%">
Called from <a href="https://docs.microsoft.com/windows/desktop/api/imepad/nn-imepad-iimepad">IImePad</a> to terminate <b>IImePadApplet</b> when the IMEPad instance exits.

</td>
</tr>
</table> 

