---
UID: NF:tom.ITextRow.GetKeepWithNext
title: ITextRow::GetKeepWithNext
author: windows-sdk-content
description: Gets whether this row should appear on the same page as the row that follows it.
old-location: controls\itextrow_getkeepwithnext.htm
tech.root: Controls
ms.assetid: 67c5f06c-9f45-430b-ae9f-0ca1931df411
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: GetKeepWithNext, GetKeepWithNext method [Windows Controls], GetKeepWithNext method [Windows Controls],ITextRow interface, ITextRow interface [Windows Controls],GetKeepWithNext method, ITextRow.GetKeepWithNext, ITextRow::GetKeepWithNext, controls.itextrow_getkeepwithnext, tom/ITextRow::GetKeepWithNext
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
 - ITextRow.GetKeepWithNext
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextRow::GetKeepWithNext


## -description


Gets  whether this row should appear on the same page as the row that follows it.


## -parameters




### -param pValue [out, retval]

Type: <b>long*</b>

A <a href="https://msdn.microsoft.com/en-us/library/Bb787724(v=VS.85).aspx">tomBool</a> value that indicates whether this row should be kept on the same page as the following row.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/49f5ffc1-d615-4d07-9f41-1c5f0dd9045b">ITextRow</a>



<a href="https://msdn.microsoft.com/9b73ca91-39a1-4dee-8414-57ee45653c07">ITextRow::SetKeepWithNext</a>
 

 

