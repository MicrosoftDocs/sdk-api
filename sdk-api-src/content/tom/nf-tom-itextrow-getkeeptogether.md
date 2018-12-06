---
UID: NF:tom.ITextRow.GetKeepTogether
title: ITextRow::GetKeepTogether
author: windows-sdk-content
description: Gets whether this row is allowed to be broken across pages.
old-location: controls\itextrow_getkeeptogether.htm
tech.root: controls
ms.assetid: 3f40c910-2636-4412-ae05-7a630c1f4806
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetKeepTogether, GetKeepTogether method [Windows Controls], GetKeepTogether method [Windows Controls],ITextRow interface, ITextRow interface [Windows Controls],GetKeepTogether method, ITextRow.GetKeepTogether, ITextRow::GetKeepTogether, controls.itextrow_getkeeptogether, tom/ITextRow::GetKeepTogether
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
 - ITextRow.GetKeepTogether
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextRow::GetKeepTogether


## -description


Gets whether this row is allowed to be broken across pages.


## -parameters




### -param pValue [out, retval]

Type: <b>long*</b>

A <a href="About_Text_Object_Model.htm">tomBool</a> value that indicates whether this row can be broken across pages.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/49f5ffc1-d615-4d07-9f41-1c5f0dd9045b">ITextRow</a>



<a href="https://msdn.microsoft.com/ca2130b4-3e29-43d7-b03d-a6c45897e447">ITextRow::SetKeepTogether</a>
 

 

