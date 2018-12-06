---
UID: NF:tom.ITextDocument2.GetStrings
title: ITextDocument2::GetStrings
author: windows-sdk-content
description: Gets a collection of rich-text strings.
old-location: controls\itextdocument2_getstrings.htm
tech.root: controls
ms.assetid: 54d8c682-4e30-4ce2-baa1-d89e28491015
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetStrings, GetStrings method [Windows Controls], GetStrings method [Windows Controls],ITextDocument2 interface, ITextDocument2 interface [Windows Controls],GetStrings method, ITextDocument2.GetStrings, ITextDocument2::GetStrings, controls.itextdocument2_getstrings, tom/ITextDocument2::GetStrings
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
 - ITextDocument2.GetStrings
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextDocument2::GetStrings


## -description


Gets a collection of rich-text strings.


## -parameters




### -param ppStrs [out]

Type: <b><a href="https://msdn.microsoft.com/c878d0db-ac13-4ac9-8601-d1c1ba76cd85">ITextStrings</a>**</b>

The collection of rich-text strings.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



The collection is useful for manipulating rich text, particularly for transforming mathematical text from linear to built-up form, or vice versa.




## -see-also




<a href="https://msdn.microsoft.com/0b0a54d7-7606-41f6-b8be-6367d9180ef4">ITextDocument2</a>
 

 

