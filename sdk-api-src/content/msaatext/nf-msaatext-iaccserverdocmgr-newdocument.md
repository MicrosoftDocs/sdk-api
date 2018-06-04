---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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



