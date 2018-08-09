---
UID: NF:textserv.ITextServices.TxGetCachedSize
title: ITextServices::TxGetCachedSize
author: windows-sdk-content
description: Returns the cached drawing logical size (if any) that text services is using. Typically, this will be the size of the last client rectangle used in ITextServices::TxDraw, ITextServices::OnTxSetCursor, and so forth, although it is not guaranteed to be.
old-location: controls\ITextServices_TxGetCachedSize.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\richedit\windowlessricheditcontrols\windowlessricheditcontrolsreference\windowlessricheditcontrolinterfaces\txgetcachedsize.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ITextServices interface [Windows Controls],TxGetCachedSize method, ITextServices.TxGetCachedSize, ITextServices::TxGetCachedSize, TxGetCachedSize, TxGetCachedSize method [Windows Controls], TxGetCachedSize method [Windows Controls],ITextServices interface, _win32_ITextServices_TxGetCachedSize, _win32_ITextServices_TxGetCachedSize_cpp, controls.ITextServices_TxGetCachedSize, controls._win32_ITextServices_TxGetCachedSize, textserv/ITextServices::TxGetCachedSize
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
 - ITextServices.TxGetCachedSize
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextServices::TxGetCachedSize


## -description


Returns the cached drawing logical size (if any) that text services is using. Typically, this will be the size of the last client rectangle used in <a href="https://msdn.microsoft.com/5fb14a41-2e73-4760-ba77-f1bfd2a1184b">ITextServices::TxDraw</a>, <a href="https://msdn.microsoft.com/9656a2ed-bd66-4083-a2b4-c6255f136f9d">ITextServices::OnTxSetCursor</a>, and so forth, although it is not guaranteed to be. 


## -parameters




### -param pdwWidth [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a>*</b>

The width, in client coordinates. 


### -param pdwHeight [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a>*</b>

The height (in client coordinates). 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, the return value is an <b>HRESULT</b> code.




## -remarks



This method can free the host from the need to maintain the cached drawing size information and the need to keep in synchronization.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/b0bc844f-2d20-4e67-84c5-0a5313bf6dee">ITextServices</a>



<a href="https://msdn.microsoft.com/9656a2ed-bd66-4083-a2b4-c6255f136f9d">OnTxSetCursor</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/5fb14a41-2e73-4760-ba77-f1bfd2a1184b">TxDraw</a>



<a href="https://msdn.microsoft.com/71ecd220-ab1a-4caa-b1b9-0951e943692e">Windowless Rich Edit Controls</a>
 

 

