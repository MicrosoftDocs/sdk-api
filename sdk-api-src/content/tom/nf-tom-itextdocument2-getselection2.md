---
UID: NF:tom.ITextDocument2.GetSelection2
title: ITextDocument2::GetSelection2
author: windows-sdk-content
description: Gets the active selection.
old-location: controls\itextdocument2_getselection2.htm
tech.root: controls
ms.assetid: a81fde9e-aef8-49cf-88b2-d0416195d70a
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: GetSelection2, GetSelection2 method [Windows Controls], GetSelection2 method [Windows Controls],ITextDocument2 interface, ITextDocument2 interface [Windows Controls],GetSelection2 method, ITextDocument2.GetSelection2, ITextDocument2::GetSelection2, controls.itextdocument2_getselection2, tom/ITextDocument2::GetSelection2
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
 - ITextDocument2.GetSelection2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextDocument2::GetSelection2


## -description


Gets the active selection.


## -parameters




### -param ppSel [out, retval]

Type: <b><a href="https://msdn.microsoft.com/75a4e233-6672-4407-bd68-ba8a7072b7b1">ITextSelection2</a>**</b>

The active selection. This parameter is <b>NULL</b> if the rich edit control is not in-place active.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/0b0a54d7-7606-41f6-b8be-6367d9180ef4">ITextDocument2</a>
 

 

