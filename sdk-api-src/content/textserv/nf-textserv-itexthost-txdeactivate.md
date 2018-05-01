---
UID: NF:textserv.ITextHost.TxDeactivate
title: ITextHost::TxDeactivate method
author: windows-driver-content
description: Notifies the text host that the control is now inactive.
old-location: controls\ITextHost_TxDeactivate.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\richedit\windowlessricheditcontrols\windowlessricheditcontrolsreference\windowlessricheditcontrolinterfaces\txdeactivate.htm
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: ITextHost, ITextHost interface [Windows Controls], TxDeactivate method, ITextHost::TxDeactivate, TxDeactivate method [Windows Controls], TxDeactivate method [Windows Controls], ITextHost interface, TxDeactivate,ITextHost.TxDeactivate, _win32_ITextHost_TxDeactivate, _win32_ITextHost_TxDeactivate_cpp, controls.ITextHost_TxDeactivate, controls._win32_ITextHost_TxDeactivate, textserv/ITextHost::TxDeactivate
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
req.typenames: TMGR_DIRECTION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Msftedit.dll
api_name:
-	ITextHost.TxDeactivate
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextHost::TxDeactivate method


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
 

 

