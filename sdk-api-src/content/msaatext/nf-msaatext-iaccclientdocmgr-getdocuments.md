---
UID: NF:msaatext.IAccClientDocMgr.GetDocuments
title: IAccClientDocMgr::GetDocuments
author: windows-sdk-content
description: Clients call IAccClientDocMgr::GetDocuments to get a list of all documents that have been registered with the Microsoft Active Accessibility run time.
old-location: winauto\iaccclientdocmgr_iaccclientdocmgr__getdocuments.htm
tech.root: WinAuto
ms.assetid: 490a202b-1fb4-4f2e-a8f2-f9134a8a9daf
ms.author: windowssdkdev
ms.date: 10/16/2018
ms.keywords: GetDocuments, GetDocuments method [Windows Accessibility], GetDocuments method [Windows Accessibility],IAccClientDocMgr interface, IAccClientDocMgr interface [Windows Accessibility],GetDocuments method, IAccClientDocMgr.GetDocuments, IAccClientDocMgr::GetDocuments, _msaa_IAccClientDocMgr_GetDocuments, msaa.iaccclientdocmgr_iaccclientdocmgr__getdocuments, msaatext/IAccClientDocMgr::GetDocuments, winauto.iaccclientdocmgr_iaccclientdocmgr__getdocuments
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
 - IAccClientDocMgr.GetDocuments
product: Windows
targetos: Windows
req.typenames: 
req.redist: Active Accessibility 2.0 RDK on Windows NT 4.0 with SP6 and later and Windows 98
---

# IAccClientDocMgr::GetDocuments


## -description


Clients call <b>IAccClientDocMgr::GetDocuments</b> to get a list of all documents that have been registered with the Microsoft Active Accessibility run time.
<div class="alert"><b>Note</b>  Active Accessibility Text Services is deprecated. Please see     
<a href="http://go.microsoft.com/fwlink/p/?linkid=131573">Microsoft Windows Text Services Framework</a>for more information on advanced text input and natural language technologies.
		</div><div> </div>

## -parameters




### -param enumUnknown [out]

Type: <b>IEnumUnknown*</b>

A list of document interface pointers.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If successful, returns S_OK.




## -remarks



Servers might need to poll this method more than once before they receive a document. There can be a limited time lapse (approximately second) between when a document appears in the system and when it is registered with document services.



