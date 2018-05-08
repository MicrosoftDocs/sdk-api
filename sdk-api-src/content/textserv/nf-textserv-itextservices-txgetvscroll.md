---
UID: NF:textserv.ITextServices.TxGetVScroll
title: ITextServices::TxGetVScroll
author: windows-driver-content
description: Returns vertical scroll bar state information.
old-location: controls\ITextServices_TxGetVScroll.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\richedit\windowlessricheditcontrols\windowlessricheditcontrolsreference\windowlessricheditcontrolinterfaces\txgetvscroll.htm
ms.author: windowsdriverdev
ms.date: 4/27/2018
ms.keywords: ITextServices interface [Windows Controls],TxGetVScroll method, ITextServices.TxGetVScroll, ITextServices::TxGetVScroll, TxGetVScroll, TxGetVScroll method [Windows Controls], TxGetVScroll method [Windows Controls],ITextServices interface, _win32_ITextServices_TxGetVScroll, _win32_ITextServices_TxGetVScroll_cpp, controls.ITextServices_TxGetVScroll, controls._win32_ITextServices_TxGetVScroll, textserv/ITextServices::TxGetVScroll
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
-	ITextServices.TxGetVScroll
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextServices::TxGetVScroll


## -description


Returns vertical scroll bar state information.


## -parameters




### -param plMin

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LONG</a>*</b>

The minimum scroll position. 


### -param plMax

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LONG</a>*</b>

The maximum scroll position. 


### -param plPos

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LONG</a>*</b>

The current scroll position. 


### -param plPage

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LONG</a>*</b>

The height of view in pixels. 


### -param pfEnabled

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a>*</b>

Indicates whether the vertical scroll bar is enabled. If <b>TRUE</b>, the vertical scroll bar is enabled; otherwise it is disabled. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, the return value is <b>S_OK</b>.

If the method fails, the return value is one of the following <b>HRESULT</b> codes. For more information on COM error codes, see <a href="https://msdn.microsoft.com/15f3ae3e-1794-4948-a7aa-6309a703364b">Error Handling in COM</a>.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more arguments are not valid.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/b0bc844f-2d20-4e67-84c5-0a5313bf6dee">ITextServices</a>



<a href="https://msdn.microsoft.com/71ecd220-ab1a-4caa-b1b9-0951e943692e">Windowless Rich Edit Controls Overview</a>
 

 

