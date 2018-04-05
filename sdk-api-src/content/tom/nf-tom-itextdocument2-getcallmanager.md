---
UID: NF:tom.ITextDocument2.GetCallManager
title: ITextDocument2::GetCallManager method
author: windows-driver-content
description: Gets the call manager.
old-location: controls\itextdocument2_getcallmanager.htm
old-project: Controls
ms.assetid: 0a90e6f5-1231-45fc-868f-4f24ed195638
ms.author: windowsdriverdev
ms.date: 3/31/2018
ms.keywords: GetCallManager method [Windows Controls], GetCallManager method [Windows Controls], ITextDocument2 interface, GetCallManager,ITextDocument2.GetCallManager, ITextDocument2, ITextDocument2 interface [Windows Controls], GetCallManager method, ITextDocument2::GetCallManager, controls.itextdocument2_getcallmanager, tom/ITextDocument2::GetCallManager
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: tom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MANCODE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Msftedit.dll
api_name:
-	ITextDocument2.GetCallManager
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextDocument2::GetCallManager method


## -description


Gets the call manager.


## -parameters




### -param ppVoid [out, retval]

Type: <b>IUnknown**</b>

The call manager object.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



The call manager object is opaque to the caller. The Text Object Model (TOM) engine uses the object to handle internal notifications for particular scenarios.




## -see-also




<a href="https://msdn.microsoft.com/0b0a54d7-7606-41f6-b8be-6367d9180ef4">ITextDocument2</a>



<a href="https://msdn.microsoft.com/4d17fdcb-502c-43ab-9f74-7247a1f14f45">ITextDocument2::ReleaseCallManager</a>
 

 

