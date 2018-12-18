---
UID: NF:textserv.ITextHost.TxGetSysColor
title: ITextHost::TxGetSysColor
author: windows-sdk-content
description: Retrieves the text host's color for a specified display element.
old-location: controls\ITextHost_TxGetSysColor.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\richedit\windowlessricheditcontrols\windowlessricheditcontrolsreference\windowlessricheditcontrolinterfaces\itexthost\itexthosttxgetsyscolor.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITextHost interface [Windows Controls],TxGetSysColor method, ITextHost.TxGetSysColor, ITextHost::TxGetSysColor, TxGetSysColor, TxGetSysColor method [Windows Controls], TxGetSysColor method [Windows Controls],ITextHost interface, _win32_ITextHost_TxGetSysColor, _win32_ITextHost_TxGetSysColor_cpp, controls.ITextHost_TxGetSysColor, controls._win32_ITextHost_TxGetSysColor, textserv/ITextHost::TxGetSysColor
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
 - ITextHost.TxGetSysColor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextHost::TxGetSysColor


## -description


Retrieves the text host's color for a specified display element.


## -parameters




### -param nIndex [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">INT</a></b>

The display element whose color is to be retrieved. For a list of possible values for this parameter, see the <a href="https://msdn.microsoft.com/165c1781-161e-4ab2-98c9-eec4e9098d09">GetSysColor</a> function. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">COLORREF</a></b>

The  value that identifies the red, green, and blue (RGB) color value of the specified element.




## -remarks



Note that the color returned may be 
				<i>different</i> than the color that would be returned from a call to <a href="https://msdn.microsoft.com/165c1781-161e-4ab2-98c9-eec4e9098d09">GetSysColor</a>. This is the case if the host overrides the default system behavior.

<div class="alert"><b>Note</b>  Hosts should be careful about overriding normal system behavior because it can result in inconsistent UI (particularly with respect to Accessibility options).</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb787615(v=VS.85).aspx">ITextHost</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb787609(v=VS.85).aspx">Windowless Rich Edit Controls Overview</a>
 

 

