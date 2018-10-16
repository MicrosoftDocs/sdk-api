---
UID: NF:tom.ITextRange2.GetDuplicate2
title: ITextRange2::GetDuplicate2
author: windows-sdk-content
description: Gets a duplicate of a range object.
old-location: controls\itextrange2_getduplicate2.htm
tech.root: controls
ms.assetid: 6dce56b6-463a-49d4-8e4b-397e2841544c
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: GetDuplicate2, GetDuplicate2 method [Windows Controls], GetDuplicate2 method [Windows Controls],ITextRange2 interface, ITextRange2 interface [Windows Controls],GetDuplicate2 method, ITextRange2.GetDuplicate2, ITextRange2::GetDuplicate2, controls.itextrange2_getduplicate2, tom/ITextRange2::GetDuplicate2
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
 - ITextRange2.GetDuplicate2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextRange2::GetDuplicate2


## -description


Gets a duplicate of a range object.


## -parameters




### -param ppRange [out, retval]

Type: <b>ITextRange2**</b>

The duplicate range.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



If this range is an <a href="https://msdn.microsoft.com/75a4e233-6672-4407-bd68-ba8a7072b7b1">ITextSelection2</a> object, the duplicate returned is an <a href="https://msdn.microsoft.com/905f0967-8b99-45ed-a1cc-19d49e919a65">ITextRange2</a> object. See the <a href="https://msdn.microsoft.com/e0c95f5b-e147-4c1f-ae1a-def36b0be5c1">ITextRange::FindText</a> method for more information. 




## -see-also




<a href="https://msdn.microsoft.com/905f0967-8b99-45ed-a1cc-19d49e919a65">ITextRange2</a>
 

 

