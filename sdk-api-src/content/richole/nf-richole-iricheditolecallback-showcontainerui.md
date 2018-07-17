---
UID: NF:richole.IRichEditOleCallback.ShowContainerUI
title: IRichEditOleCallback::ShowContainerUI
author: windows-sdk-content
description: Indicates whether or not the application is to display its container UI.
old-location: controls\IRichEditOleCallback_ShowContainerUI.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\richedit\richeditcontrols\richeditcontrolreference\richeditinterfaces\iricheditolecallback\iricheditolecallbackshowcontainerui.htm
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: IRichEditOleCallback interface [Windows Controls],ShowContainerUI method, IRichEditOleCallback.ShowContainerUI, IRichEditOleCallback::ShowContainerUI, ShowContainerUI, ShowContainerUI method [Windows Controls], ShowContainerUI method [Windows Controls],IRichEditOleCallback interface, _win32_IRichEditOleCallback_ShowContainerUI, _win32_IRichEditOleCallback_ShowContainerUI_cpp, controls.IRichEditOleCallback_ShowContainerUI, controls._win32_IRichEditOleCallback_ShowContainerUI, richole/IRichEditOleCallback::ShowContainerUI
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: TEXTRANGEW
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msftedit.dll
api_name:
 - IRichEditOleCallback.ShowContainerUI
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: ADAM
---

# IRichEditOleCallback::ShowContainerUI


## -description


Indicates whether or not the application is to display its container UI. The rich edit control looks ahead for double-clicks and defers the call if appropriate. Applications may defer hiding adornments until an <a href="https://msdn.microsoft.com/7c806a02-db6d-444e-a049-22c4ae2b19b0">IOleInPlaceUIWindow::SetBorderSpace</a> call is received.


## -parameters




### -param fShow

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Show container UI flag. The value is <b>TRUE</b> if the container UI is displayed, and <b>FALSE</b> if it is not. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

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
				<b>IRichEditOleCallback::ShowContainerUI</b> method is called by the <a href="https://msdn.microsoft.com/d863805c-58c1-4e35-84b5-72f01a4ba205">IOleInPlaceSite::OnUIActivate</a> and <a href="https://msdn.microsoft.com/926c02b4-0bfa-4509-b5bc-4e5007e4db1a">IOleInPlaceSite::OnUIDeactivate</a> methods of the <a href="https://msdn.microsoft.com/6d37e022-8c19-48b3-affb-e0eca19b5e05">IOleInPlaceSite</a> interface. 




## -see-also




<a href="https://msdn.microsoft.com/c530aff7-fd83-413d-8945-0c9d1bfb51ba">IOleInPlaceFrame</a>



<a href="https://msdn.microsoft.com/2c3ba341-f62f-4c95-9547-6d50fcf3d6b4">IRichEditOleCallback</a>



<b>Other Resources</b>



<b>Reference</b>
 

 

