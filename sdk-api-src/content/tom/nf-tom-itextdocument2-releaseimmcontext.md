---
UID: NF:tom.ITextDocument2.ReleaseImmContext
title: ITextDocument2::ReleaseImmContext
author: windows-sdk-content
description: Releases an Input Method Manager (IMM) input context.
old-location: controls\itextdocument2_releaseimmcontext.htm
tech.root: Controls
ms.assetid: 2172e20b-2343-4a65-a08e-0d8b8c101860
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: ITextDocument2 interface [Windows Controls],ReleaseImmContext method, ITextDocument2.ReleaseImmContext, ITextDocument2::ReleaseImmContext, ReleaseImmContext, ReleaseImmContext method [Windows Controls], ReleaseImmContext method [Windows Controls],ITextDocument2 interface, controls.itextdocument2_releaseimmcontext, tom/ITextDocument2::ReleaseImmContext
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
 - ITextDocument2.ReleaseImmContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextDocument2::ReleaseImmContext


## -description


Releases an Input Method Manager (IMM) input context.


## -parameters




### -param Context [in]

Type: <b>int64</b>

The IMM input context to release.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/0b0a54d7-7606-41f6-b8be-6367d9180ef4">ITextDocument2</a>



<a href="https://msdn.microsoft.com/42ee6d71-b51d-459a-b1af-638a19d8be2c">ITextDocument2::GetIMMContext</a>
 

 

