---
UID: NF:textserv.ITextHost.TxGetExtent
title: ITextHost::TxGetExtent
author: windows-sdk-content
description: Requests the native size of the control in HIMETRIC.
old-location: controls\ITextHost_TxGetExtent.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\richedit\windowlessricheditcontrols\windowlessricheditcontrolsreference\windowlessricheditcontrolinterfaces\txgetextent.htm
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: ITextHost interface [Windows Controls],TxGetExtent method, ITextHost.TxGetExtent, ITextHost::TxGetExtent, TxGetExtent, TxGetExtent method [Windows Controls], TxGetExtent method [Windows Controls],ITextHost interface, _win32_ITextHost_TxGetExtent, _win32_ITextHost_TxGetExtent_cpp, controls.ITextHost_TxGetExtent, controls._win32_ITextHost_TxGetExtent, textserv/ITextHost::TxGetExtent
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: textserv.h
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
 - ITextHost.TxGetExtent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- textserv.h
: 
- ITextHost.TxGetExtent
: 
---

# ITextHost::TxGetExtent


## -description


Requests the native size of the control in HIMETRIC.


## -parameters




### -param lpExtent

Type: <b>LPSIZEL</b>

The size of the control in HIMETRIC, that is, where the unit is .01 millimeter. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

Return S_OK if the method succeeds. 

Return the following COM error code if the method fails. For more information on COM error codes, see <a href="https://msdn.microsoft.com/15f3ae3e-1794-4948-a7aa-6309a703364b">Error Handling in COM</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Not implemented. 

</td>
</tr>
</table>
 




## -remarks



This method is used by the text services object to implement zooming. The text services object derives the zoom factor from the ratio between the himetric and device pixel extent of the client rectangle. Each HIMETRIC unit corresponds to 0.01 millimeter.

[vertical zoom factor] = [pixel height of the client rect] * 2540 / [HIMETRIC vertical extent] * [pixel per vertical inch (from device context)]

If the vertical and horizontal zoom factors are not the same, the text services object can ignore the horizontal zoom factor and assume it is the same as the vertical one.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/28d86b94-2d36-4749-8954-3857bf6dbdac">ITextHost</a>



<b>Other Resources</b>



<a href="https://msdn.microsoft.com/8cb0802c-1868-4f3b-8287-c6fb1fa7ab68">SIZE</a>



<a href="https://msdn.microsoft.com/71ecd220-ab1a-4caa-b1b9-0951e943692e">Windowless Rich Edit Controls</a>
 

 

