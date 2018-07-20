---
UID: NF:textserv.ITextHost.TxGetPropertyBits
title: ITextHost::TxGetPropertyBits
author: windows-sdk-content
description: Requests the bit property settings for the text host.
old-location: controls\ITextHost_TxGetPropertyBits.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\richedit\windowlessricheditcontrols\windowlessricheditcontrolsreference\windowlessricheditcontrolinterfaces\itexthost\itexthosttxgetpropertybits.htm
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: ITextHost interface [Windows Controls],TxGetPropertyBits method, ITextHost.TxGetPropertyBits, ITextHost::TxGetPropertyBits, TxGetPropertyBits, TxGetPropertyBits method [Windows Controls], TxGetPropertyBits method [Windows Controls],ITextHost interface, _win32_ITextHost_TxGetPropertyBits, _win32_ITextHost_TxGetPropertyBits_cpp, controls.ITextHost_TxGetPropertyBits, controls._win32_ITextHost_TxGetPropertyBits, textserv/ITextHost::TxGetPropertyBits
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
 - ITextHost.TxGetPropertyBits
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextHost::TxGetPropertyBits


## -description


Requests the bit property settings for the text host.


## -parameters




### -param dwMask [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Mask of properties in which the caller is interested. For the possible bit values, see 
					<i>dwBits</i> in <a href="https://msdn.microsoft.com/library/Bb787627(v=VS.85).aspx">OnTxPropertyBitsChange</a>. 


### -param pdwBits [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a>*</b>

The current settings for the properties specified by 
					<i>dwMask</i>. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

The return value is <b>S_OK</b>.




## -remarks



This call is valid at any time, for any combination of requested property bits. 




## -see-also




<a href="https://msdn.microsoft.com/library/Bb787615(v=VS.85).aspx">ITextHost</a>



<a href="https://msdn.microsoft.com/library/Bb787609(v=VS.85).aspx">Windowless Rich Edit Controls Overview</a>
 

 

