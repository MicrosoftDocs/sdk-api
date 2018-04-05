---
UID: NF:tom.ITextRange2.DeleteSubrange
title: ITextRange2::DeleteSubrange method
author: windows-driver-content
description: Deletes a subrange from a range.
old-location: controls\itextrange2_deletesubrange.htm
old-project: Controls
ms.assetid: ad75725d-ad92-45fc-a0a9-3227bfb99284
ms.author: windowsdriverdev
ms.date: 3/31/2018
ms.keywords: DeleteSubrange method [Windows Controls], DeleteSubrange method [Windows Controls], ITextRange2 interface, DeleteSubrange,ITextRange2.DeleteSubrange, ITextRange2, ITextRange2 interface [Windows Controls], DeleteSubrange method, ITextRange2::DeleteSubrange, controls.itextrange2_deletesubrange, tom/ITextRange2::DeleteSubrange
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
-	ITextRange2.DeleteSubrange
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextRange2::DeleteSubrange method


## -description


Deletes a subrange from a range. 


## -parameters




### -param cpFirst [in]

Type: <b>long</b>

The start character position of the subrange.


### -param cpLim [in]

Type: <b>long</b>

The end character position of the subrange.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/905f0967-8b99-45ed-a1cc-19d49e919a65">ITextRange2</a>
 

 

