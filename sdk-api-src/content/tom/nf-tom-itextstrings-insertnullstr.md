---
UID: NF:tom.ITextStrings.InsertNullStr
title: ITextStrings::InsertNullStr
author: windows-sdk-content
description: Inserts a NULL string in the collection at a selected string index.
old-location: controls\itextstrings_insertnullstr.htm
tech.root: controls
ms.assetid: dc269f41-f65c-4335-ac5c-5c57187f20aa
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITextStrings interface [Windows Controls],InsertNullStr method, ITextStrings.InsertNullStr, ITextStrings::InsertNullStr, InsertNullStr, InsertNullStr method [Windows Controls], InsertNullStr method [Windows Controls],ITextStrings interface, controls.itextstrings_insertnullstr, tom/ITextStrings::InsertNullStr
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
 - ITextStrings.InsertNullStr
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextStrings::InsertNullStr


## -description


Inserts a <b>NULL</b> string in the collection at a selected string index.


## -parameters




### -param iString [in]

Type: <b>long</b>

The string index.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



The index is relative to the top of the collection, so <i>iString</i> = 0 inserts the <b>NULL</b> string at the top, <i>iString</i> = –1 inserts it below the top string, and so on.




## -see-also




<a href="https://msdn.microsoft.com/c878d0db-ac13-4ac9-8601-d1c1ba76cd85">ITextStrings</a>
 

 

