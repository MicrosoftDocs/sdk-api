---
UID: NF:textserv.ITextHost.TxReleaseDC
title: ITextHost::TxReleaseDC
author: windows-sdk-content
description: Releases the device context obtained by the ITextHost::TxGetDC method.
old-location: controls\ITextHost_TxReleaseDC.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\richedit\windowlessricheditcontrols\windowlessricheditcontrolsreference\windowlessricheditcontrolinterfaces\itexthost\itexthosttxreleasedc.htm
ms.author: windowssdkdev
ms.date: 06/29/2018
ms.keywords: ITextHost interface [Windows Controls],TxReleaseDC method, ITextHost.TxReleaseDC, ITextHost::TxReleaseDC, TxReleaseDC, TxReleaseDC method [Windows Controls], TxReleaseDC method [Windows Controls],ITextHost interface, _win32_ITextHost_TxReleaseDC, _win32_ITextHost_TxReleaseDC_cpp, controls.ITextHost_TxReleaseDC, controls._win32_ITextHost_TxReleaseDC, textserv/ITextHost::TxReleaseDC
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
 - ITextHost.TxReleaseDC
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextHost::TxReleaseDC


## -description


Releases the device context obtained by the <a href="https://msdn.microsoft.com/library/Bb787660(v=VS.85).aspx">ITextHost::TxGetDC</a> method.


## -parameters




### -param hdc [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HDC</a></b>

Handle to the device context to release. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">INT</a></b>

Returns 1 if <i>hdc</i> was released; otherwise 0.
                    

For more information on COM error codes, see <a href="https://msdn.microsoft.com/15f3ae3e-1794-4948-a7aa-6309a703364b">Error Handling in COM</a>.




## -remarks



This method is only valid when the control is in-place active; calls while the control is inactive may fail.




## -see-also




<a href="https://msdn.microsoft.com/library/Bb787615(v=VS.85).aspx">ITextHost</a>



<a href="https://msdn.microsoft.com/library/Bb787609(v=VS.85).aspx">Windowless Rich Edit Controls Overview</a>
 

 

