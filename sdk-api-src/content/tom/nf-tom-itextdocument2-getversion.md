---
UID: NF:tom.ITextDocument2.GetVersion
title: ITextDocument2::GetVersion
author: windows-sdk-content
description: Gets the version number of the Text Object Model (TOM) engine.
old-location: controls\itextdocument2_getversion.htm
tech.root: controls
ms.assetid: 4cc4502b-4e7c-4561-b7d4-a248bf248a8a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetVersion, GetVersion method [Windows Controls], GetVersion method [Windows Controls],ITextDocument2 interface, ITextDocument2 interface [Windows Controls],GetVersion method, ITextDocument2.GetVersion, ITextDocument2::GetVersion, controls.itextdocument2_getversion, tom/ITextDocument2::GetVersion
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
 - ITextDocument2.GetVersion
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextDocument2::GetVersion


## -description


Gets the version number of the Text Object Model (TOM) engine.


## -parameters




### -param pValue [out, retval]

Type: <b>long*</b>

The version number. Byte 3 gives the major version number, byte 2 the minor version number, and the low-order 16 bits give the build number.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/0b0a54d7-7606-41f6-b8be-6367d9180ef4">ITextDocument2</a>



<a href="https://msdn.microsoft.com/22cfa44e-3603-458b-991e-6e536df63803">ITextDocument2::GetGenerator</a>
 

 

