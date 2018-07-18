---
UID: NF:textserv.ITextHost.TxDeactivate
title: ITextHost::TxDeactivate
author: windows-sdk-content
description: Notifies the text host that the control is now inactive.
old-location: controls\ITextHost_TxDeactivate.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\richedit\windowlessricheditcontrols\windowlessricheditcontrolsreference\windowlessricheditcontrolinterfaces\txdeactivate.htm
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: ITextHost interface [Windows Controls],TxDeactivate method, ITextHost.TxDeactivate, ITextHost::TxDeactivate, TxDeactivate, TxDeactivate method [Windows Controls], TxDeactivate method [Windows Controls],ITextHost interface, _win32_ITextHost_TxDeactivate, _win32_ITextHost_TxDeactivate_cpp, controls.ITextHost_TxDeactivate, controls._win32_ITextHost_TxDeactivate, textserv/ITextHost::TxDeactivate
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: TMGR_DIRECTION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msftedit.dll
api_name:
 - ITextHost.TxDeactivate
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextHost::TxDeactivate


## -description


Notifies the text host that the control is now inactive.


## -parameters




### -param lNewState

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LONG</a></b>

New state of the control. Typically it is the value returned by <a href="https://msdn.microsoft.com/3ad31706-e5aa-49ea-8416-ce522fbdfbac">ITextHost::TxActivate</a>. 


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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Unspecified error.

</td>
</tr>
</table>
 




## -remarks



No matter how many times this method is called, only one call to <a href="https://msdn.microsoft.com/3ad31706-e5aa-49ea-8416-ce522fbdfbac">ITextHost::TxActivate</a> is necessary to activate the control.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/28d86b94-2d36-4749-8954-3857bf6dbdac">ITextHost</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/3ad31706-e5aa-49ea-8416-ce522fbdfbac">TxActivate</a>



<a href="https://msdn.microsoft.com/71ecd220-ab1a-4caa-b1b9-0951e943692e">Windowless Rich Edit Controls</a>
 

 

