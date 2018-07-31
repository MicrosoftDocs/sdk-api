---
UID: NF:tom.ITextDocument2.RangeFromPoint2
title: ITextDocument2::RangeFromPoint2
author: windows-sdk-content
description: Retrieves the degenerate range at (or nearest to) a particular point on the screen.
old-location: controls\itextdocument2_rangefrompoint2.htm
old-project: Controls
ms.assetid: 3212c6cc-a1fb-44ca-aba9-2234414e7a39
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: ITextDocument2 interface [Windows Controls],RangeFromPoint2 method, ITextDocument2.RangeFromPoint2, ITextDocument2::RangeFromPoint2, RangeFromPoint2, RangeFromPoint2 method [Windows Controls], RangeFromPoint2 method [Windows Controls],ITextDocument2 interface, controls.itextdocument2_rangefrompoint2, tom/ITextDocument2::RangeFromPoint2
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
 - ITextDocument2.RangeFromPoint2
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextDocument2::RangeFromPoint2


## -description


Retrieves the degenerate range at (or nearest to) a particular point on the screen.


## -parameters




### -param x [in]

Type: <b>long</b>

The x-coordinate of a point, in screen coordinates.


### -param y [in]

Type: <b>long</b>

The y-coordinate of a point, in screen coordinates.


### -param Type [in]

Type: <b>long</b>

The alignment type of the specified point. For a list of valid values, see <a href="https://msdn.microsoft.com/en-us/library/Bb774003(v=VS.85).aspx">ITextRange::GetPoint</a>.


### -param ppRange [out, retval]

Type: <b>ITextRange2**</b>


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/0b0a54d7-7606-41f6-b8be-6367d9180ef4">ITextDocument2</a>
 

 

