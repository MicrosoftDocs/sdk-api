---
UID: NF:tom.ITextDocument2.GetDisplays
title: ITextDocument2::GetDisplays
author: windows-sdk-content
description: Gets the displays collection for this Text Object Model (TOM) engine instance.
old-location: controls\itextdocument2_getdisplays.htm
old-project: controls
ms.assetid: 8f610b45-9c17-4b20-82e0-fa78169360cc
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetDisplays, GetDisplays method [Windows Controls], GetDisplays method [Windows Controls],ITextDocument2 interface, ITextDocument2 interface [Windows Controls],GetDisplays method, ITextDocument2.GetDisplays, ITextDocument2::GetDisplays, controls.itextdocument2_getdisplays, tom/ITextDocument2::GetDisplays
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: tom.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: MANCODE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msftedit.dll
api_name:
 - ITextDocument2.GetDisplays
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextDocument2::GetDisplays


## -description


Gets the displays collection for this Text Object Model (TOM) engine instance.


## -parameters




### -param ppDisplays [out, retval]

Type: <b><a href="https://msdn.microsoft.com/e7266734-c066-4f80-8d3d-99ffb251cd39">ITextDisplays</a>**</b>

The displays collection.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



The rich edit control doesn't implement this method.




## -see-also




<a href="https://msdn.microsoft.com/0b0a54d7-7606-41f6-b8be-6367d9180ef4">ITextDocument2</a>
 

 

