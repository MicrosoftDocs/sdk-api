---
UID: NF:msaatext.IAccServerDocMgr.RevokeDocument
title: IAccServerDocMgr::RevokeDocument
author: windows-sdk-content
description: Server applications call the IAccServerDocMgr::RevokeDocument method to notify the Microsoft Active Accessibility run time that a document is no longer available. Calling RevokeDocument removes it from the store so that clients cannot see the document.
old-location: winauto\iaccserverdocmgr_iaccserverdocmgr__revokedocument.htm
tech.root: WinAuto
ms.assetid: 8691a641-fc06-451c-9988-234e01dc02df
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IAccServerDocMgr interface [Windows Accessibility],RevokeDocument method, IAccServerDocMgr.RevokeDocument, IAccServerDocMgr::RevokeDocument, RevokeDocument, RevokeDocument method [Windows Accessibility], RevokeDocument method [Windows Accessibility],IAccServerDocMgr interface, _msaa_IAccServerDocMgr_RevokeDocument, msaa.iaccserverdocmgr_iaccserverdocmgr__revokedocument, msaatext/IAccServerDocMgr::RevokeDocument, winauto.iaccserverdocmgr_iaccserverdocmgr__revokedocument
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: msaatext.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.dll: Msaatext.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msaatext.dll
api_name:
 - IAccServerDocMgr.RevokeDocument
product: Windows
targetos: Windows
req.typenames: 
req.redist: Active Accessibility 2.0 RDK on Windows NT 4.0 with SP6 and later and Windows 98
- apiref
: 
- COM
: 
- msaatext.h
: 
- IAccServerDocMgr.RevokeDocument
: 
---

# IAccServerDocMgr::RevokeDocument


## -description


Server applications call the <b>IAccServerDocMgr::RevokeDocument</b> method to notify the Microsoft Active Accessibility run time that a document is no longer available. Calling <b>RevokeDocument</b> removes it from the store so that clients cannot see the document.
<div class="alert"><b>Note</b>  Active Accessibility Text Services is deprecated. Please see     
<a href="https://go.microsoft.com/fwlink/p/?linkid=131573">Microsoft Windows Text Services Framework</a>for more information on advanced text input and natural language technologies.
		</div><div> </div>

## -parameters




### -param punk [in]

Type: <b>IUnknown*</b>

An interface pointer to the document being revoked.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If successful, returns S_OK.



