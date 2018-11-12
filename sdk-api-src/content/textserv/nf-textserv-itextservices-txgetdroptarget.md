---
UID: NF:textserv.ITextServices.TxGetDropTarget
title: ITextServices::TxGetDropTarget
author: windows-sdk-content
description: Gets the drop target for the text control.
old-location: controls\ITextServices_TxGetDropTarget.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\richedit\windowlessricheditcontrols\windowlessricheditcontrolsreference\windowlessricheditcontrolinterfaces\txgetdroptarget.htm
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: ITextServices interface [Windows Controls],TxGetDropTarget method, ITextServices.TxGetDropTarget, ITextServices::TxGetDropTarget, TxGetDropTarget, TxGetDropTarget method [Windows Controls], TxGetDropTarget method [Windows Controls],ITextServices interface, _win32_ITextServices_TxGetDropTarget, _win32_ITextServices_TxGetDropTarget_cpp, controls.ITextServices_TxGetDropTarget, controls._win32_ITextServices_TxGetDropTarget, textserv/ITextServices::TxGetDropTarget
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
 - ITextServices.TxGetDropTarget
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextServices::TxGetDropTarget


## -description


Gets the drop target for the text control.


## -parameters




### -param ppDropTarget

Type: <b><a href="https://msdn.microsoft.com/13fbe834-1ef8-4944-b2e4-9f5c413c65c8">IDropTarget</a>**</b>

The target of a drag-and-drop operation in a specified window. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method got the drop target successfully, the return value is <b>S_OK</b>.

 For more information on COM error codes, see <a href="https://msdn.microsoft.com/15f3ae3e-1794-4948-a7aa-6309a703364b">Error Handling in COM</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Could not create the drop target.

</td>
</tr>
</table>
 




## -remarks



The host (caller) is responsible for calling <a href="https://msdn.microsoft.com/00726271-4436-41f5-b7cc-666cd77216bc">RegisterDragDrop</a> or <a href="https://msdn.microsoft.com/c0fa963c-ed06-426c-8ffc-31b02f083a23">RevokeDragDrop</a>, and for calling <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">Release</a> on the returned drop target when done.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/13fbe834-1ef8-4944-b2e4-9f5c413c65c8">IDropTarget</a>



<a href="https://msdn.microsoft.com/b0bc844f-2d20-4e67-84c5-0a5313bf6dee">ITextServices</a>



<b>Other Resources</b>



<a href="https://msdn.microsoft.com/00726271-4436-41f5-b7cc-666cd77216bc">RegisterDragDrop</a>



<a href="https://msdn.microsoft.com/c0fa963c-ed06-426c-8ffc-31b02f083a23">RevokeDragDrop</a>



<a href="https://msdn.microsoft.com/71ecd220-ab1a-4caa-b1b9-0951e943692e">Windowless Rich Edit Controls</a>
 

 

