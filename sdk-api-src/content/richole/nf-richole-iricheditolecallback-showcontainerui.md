---
UID: NF:richole.IRichEditOleCallback.ShowContainerUI
title: IRichEditOleCallback::ShowContainerUI (richole.h)
description: Indicates whether or not the application is to display its container UI.
helpviewer_keywords: ["IRichEditOleCallback interface [Windows Controls]","ShowContainerUI method","IRichEditOleCallback.ShowContainerUI","IRichEditOleCallback::ShowContainerUI","ShowContainerUI","ShowContainerUI method [Windows Controls]","ShowContainerUI method [Windows Controls]","IRichEditOleCallback interface","_win32_IRichEditOleCallback_ShowContainerUI","_win32_IRichEditOleCallback_ShowContainerUI_cpp","controls.IRichEditOleCallback_ShowContainerUI","controls._win32_IRichEditOleCallback_ShowContainerUI","richole/IRichEditOleCallback::ShowContainerUI"]
old-location: controls\IRichEditOleCallback_ShowContainerUI.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\richeditcontrols\richeditcontrolreference\richeditinterfaces\iricheditolecallback\iricheditolecallbackshowcontainerui.htm
ms.date: 12/05/2018
ms.keywords: IRichEditOleCallback interface [Windows Controls],ShowContainerUI method, IRichEditOleCallback.ShowContainerUI, IRichEditOleCallback::ShowContainerUI, ShowContainerUI, ShowContainerUI method [Windows Controls], ShowContainerUI method [Windows Controls],IRichEditOleCallback interface, _win32_IRichEditOleCallback_ShowContainerUI, _win32_IRichEditOleCallback_ShowContainerUI_cpp, controls.IRichEditOleCallback_ShowContainerUI, controls._win32_IRichEditOleCallback_ShowContainerUI, richole/IRichEditOleCallback::ShowContainerUI
req.header: richole.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: Msftedit.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IRichEditOleCallback::ShowContainerUI
 - richole/IRichEditOleCallback::ShowContainerUI
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msftedit.dll
api_name:
 - IRichEditOleCallback.ShowContainerUI
---

# IRichEditOleCallback::ShowContainerUI


## -description

Indicates whether or not the application is to display its container UI. The rich edit control looks ahead for double-clicks and defers the call if appropriate. Applications may defer hiding adornments until an <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleinplaceuiwindow-setborderspace">IOleInPlaceUIWindow::SetBorderSpace</a> call is received.

## -parameters

### -param fShow

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Show container UI flag. The value is <b>TRUE</b> if the container UI is displayed, and <b>FALSE</b> if it is not.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

Returns <b>S_OK</b> on success. If the method fails, it can return the following value.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
There was an invalid argument.

</td>
</tr>
</table>

## -remarks

The 
				<b>IRichEditOleCallback::ShowContainerUI</b> method is called by the <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleinplacesite-onuiactivate">IOleInPlaceSite::OnUIActivate</a> and <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleinplacesite-onuideactivate">IOleInPlaceSite::OnUIDeactivate</a> methods of the <a href="/windows/desktop/api/oleidl/nn-oleidl-ioleinplacesite">IOleInPlaceSite</a> interface.

## -see-also

<a href="/windows/desktop/api/oleidl/nn-oleidl-ioleinplaceframe">IOleInPlaceFrame</a>



<a href="/windows/desktop/api/richole/nn-richole-iricheditolecallback">IRichEditOleCallback</a>



<b>Other Resources</b>



<b>Reference</b>