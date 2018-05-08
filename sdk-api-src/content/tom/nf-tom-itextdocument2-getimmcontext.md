---
UID: NF:tom.ITextDocument2.GetImmContext
title: ITextDocument2::GetImmContext
author: windows-driver-content
description: Gets the Input Method Manager (IMM) input context from the Text Object Model (TOM) host.
old-location: controls\itextdocument2_getimmcontext.htm
old-project: Controls
ms.assetid: 42ee6d71-b51d-459a-b1af-638a19d8be2c
ms.author: windowsdriverdev
ms.date: 4/27/2018
ms.keywords: GetImmContext, GetImmContext method [Windows Controls], GetImmContext method [Windows Controls],ITextDocument2 interface, ITextDocument2 interface [Windows Controls],GetImmContext method, ITextDocument2.GetImmContext, ITextDocument2::GetImmContext, controls.itextdocument2_getimmcontext, tom/ITextDocument2::GetImmContext
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
-	ITextDocument2.GetImmContext
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextDocument2::GetImmContext


## -description


Gets the Input Method Manager (IMM) input context from the Text Object Model (TOM) host.


## -parameters




### -param pContext [out, retval]

Type: <b>__int64*</b>

The IMM input context.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/0b0a54d7-7606-41f6-b8be-6367d9180ef4">ITextDocument2</a>



<a href="https://msdn.microsoft.com/2172e20b-2343-4a65-a08e-0d8b8c101860">ITextDocument2::ReleaseIMMContext</a>
 

 

