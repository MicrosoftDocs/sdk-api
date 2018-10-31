---
UID: NF:richole.IRichEditOleCallback.GetInPlaceContext
title: IRichEditOleCallback::GetInPlaceContext
author: windows-sdk-content
description: Provides the application and document-level interfaces and information required to support in-place activation.
old-location: controls\IRichEditOleCallback_GetInPlaceContext.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\richedit\richeditcontrols\richeditcontrolreference\richeditinterfaces\iricheditolecallback\iricheditolecallbackgetinplacecontext.htm
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: GetInPlaceContext, GetInPlaceContext method [Windows Controls], GetInPlaceContext method [Windows Controls],IRichEditOleCallback interface, IRichEditOleCallback interface [Windows Controls],GetInPlaceContext method, IRichEditOleCallback.GetInPlaceContext, IRichEditOleCallback::GetInPlaceContext, _win32_IRichEditOleCallback_GetInPlaceContext, _win32_IRichEditOleCallback_GetInPlaceContext_cpp, controls.IRichEditOleCallback_GetInPlaceContext, controls._win32_IRichEditOleCallback_GetInPlaceContext, richole/IRichEditOleCallback::GetInPlaceContext
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: Msftedit.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msftedit.dll
api_name:
 - IRichEditOleCallback.GetInPlaceContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IRichEditOleCallback::GetInPlaceContext


## -description


Provides the application and document-level interfaces and information required to support in-place activation.


## -parameters




### -param lplpFrame

Type: <b>LPOLEINPLACEFRAME*</b>

The address of the <a href="https://msdn.microsoft.com/c530aff7-fd83-413d-8945-0c9d1bfb51ba">IOleInPlaceFrame</a> interface that represents the frame window of a rich edit control client. Use the <a href="https://msdn.microsoft.com/b4316efd-73d4-4995-b898-8025a316ba63">AddRef</a> method to increment the reference count. The rich edit control releases the interface when it is no longer needed. 


### -param lplpDoc

Type: <b>LPOLEINPLACEUIWINDOW*</b>

The address of the <a href="https://msdn.microsoft.com/3cfb31aa-9746-438c-af64-8236c170fe88">IOleInPlaceUIWindow</a> interface that represents the document window of the rich edit control client. An interface need not be returned if the frame and document windows are the same. Use the <a href="https://msdn.microsoft.com/b4316efd-73d4-4995-b898-8025a316ba63">AddRef</a>method to increment the reference count. The rich edit control releases the interface when it is no longer needed. 


### -param lpFrameInfo

Type: <b>LPOLEINPLACEFRAMEINFO</b>

The accelerator information. 


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
 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb774308(v=VS.85).aspx">IRichEditOleCallback</a>
 

 

