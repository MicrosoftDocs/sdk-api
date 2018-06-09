---
UID: NF:msaatext.IAccServerDocMgr.NewDocument
title: IAccServerDocMgr::NewDocument
author: windows-sdk-content
description: Server applications call the IAccServerDocMgr::NewDocument method when it is available. The adapter creates a wrapped document and registers it with the store, so clients can access information about the text in the document.
old-location: winauto\iaccserverdocmgr_iaccserverdocmgr__newdocument.htm
old-project: WinAuto
ms.assetid: 8bac6081-3b4e-45df-a900-66bc037a232f
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: IAccServerDocMgr interface [Windows Accessibility],NewDocument method, IAccServerDocMgr.NewDocument, IAccServerDocMgr::NewDocument, NewDocument, NewDocument method [Windows Accessibility], NewDocument method [Windows Accessibility],IAccServerDocMgr interface, _msaa_IAccServerDocMgr_NewDocument, msaa.iaccserverdocmgr_iaccserverdocmgr__newdocument, msaatext/IAccServerDocMgr::NewDocument, winauto.iaccserverdocmgr_iaccserverdocmgr__newdocument
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: SSTP_CONFIG_PARAMS, *PSSTP_CONFIG_PARAMS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msaatext.dll
api_name:
 - IAccServerDocMgr.NewDocument
product: Windows
targetos: Windows
req.lib: 
req.dll: Msaatext.dll
req.irql: 
req.product: GDI+ 1.1
---

# IAccServerDocMgr::NewDocument


## -description


Server applications call the <b>IAccServerDocMgr::NewDocument</b> method when it is available. The adapter creates a wrapped document and registers it with the store, so clients can access information about the text in the document.
<div class="alert"><b>Note</b>  Active Accessibility Text Services is deprecated. Please see     
<a href="http://go.microsoft.com/fwlink/p/?linkid=131573">Microsoft Windows Text Services Framework</a>
for more information on advanced text input and natural language technologies.
		</div><div> </div>

## -parameters




### -param riid [in]

Type: <b>REFIID</b>

IID of the document. This is usually IID_ITextStoreAnchor.


### -param punk

Type: <b>IUnknown*</b>

[in, iid_is(riid)] An interface pointer to the document.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If successful, returns S_OK.




## -remarks



The server application calls the <b>IAccServerDocMgr::NewDocument</b> method to notify the Microsoft Active Accessibility run time that a document is available. Calling <b>NewDocument</b> adds the document to the Microsoft Active Accessibility store so that clients can access the document.



