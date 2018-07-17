---
UID: NF:tom.ITextDocument2.CheckTextLimit
title: ITextDocument2::CheckTextLimit
author: windows-sdk-content
description: Checks whether the number of characters to be added would exceed the maximum text limit.
old-location: controls\itextdocument2_checktextlimit.htm
old-project: Controls
ms.assetid: 2c3aae14-8fa4-47bf-93ae-1d34333f0356
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: CheckTextLimit, CheckTextLimit method [Windows Controls], CheckTextLimit method [Windows Controls],ITextDocument2 interface, ITextDocument2 interface [Windows Controls],CheckTextLimit method, ITextDocument2.CheckTextLimit, ITextDocument2::CheckTextLimit, controls.itextdocument2_checktextlimit, tom/ITextDocument2::CheckTextLimit
ms.prod: windows
ms.technology: windows-sdk
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
 - ITextDocument2.CheckTextLimit
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextDocument2::CheckTextLimit


## -description


Checks whether the number of characters to be added would exceed the maximum text limit.


## -parameters




### -param cch [in]

Type: <b>long</b>

The number of characters to be added.


### -param pcch [out]

Type: <b>long*</b>

The number of characters that exceed the maximum text limit. This parameter is 0 if the number of characters does not exceed the limit. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/0b0a54d7-7606-41f6-b8be-6367d9180ef4">ITextDocument2</a>
 

 

