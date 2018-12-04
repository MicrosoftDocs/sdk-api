---
UID: NF:tom.ITextRange2.GetCount
title: ITextRange2::GetCount
author: windows-sdk-content
description: Gets the count of subranges, including the active subrange in the current range.
old-location: controls\itextrange2_getcount.htm
tech.root: controls
ms.assetid: a1744e60-74b0-44a0-b470-6e89d328fa11
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: GetCount, GetCount method [Windows Controls], GetCount method [Windows Controls],ITextRange2 interface, ITextRange2 interface [Windows Controls],GetCount method, ITextRange2.GetCount, ITextRange2::GetCount, controls.itextrange2_getcount, tom/ITextRange2::GetCount
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
 - ITextRange2.GetCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextRange2::GetCount


## -description


Gets the count of subranges, including the  active subrange in the current range.


## -parameters




### -param pCount [out, retval]

Type: <b>long*</b>

The count of subranges not including the active one.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



If you select a  range with no or one character, the count will be 1. But if you select a word and then move to a different location, and select a second word not touching the first, then the count is 2. 

See <a href="https://msdn.microsoft.com/ffd1f166-a37c-4b39-9878-a4008260f675">ITextRange2::AddSubrange</a> to add subranges programmatically.




## -see-also




<a href="https://msdn.microsoft.com/905f0967-8b99-45ed-a1cc-19d49e919a65">ITextRange2</a>
 

 

