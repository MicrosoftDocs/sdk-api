---
UID: NF:tom.ITextStrings.MoveBoundary
title: ITextStrings::MoveBoundary
author: windows-sdk-content
description: Moves the start boundary of a string, by index, for a selected number of characters.
old-location: controls\itextstrings_moveboundary.htm
tech.root: controls
ms.assetid: db0eff33-f20a-481e-bcae-8a72674ab906
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITextStrings interface [Windows Controls],MoveBoundary method, ITextStrings.MoveBoundary, ITextStrings::MoveBoundary, MoveBoundary, MoveBoundary method [Windows Controls], MoveBoundary method [Windows Controls],ITextStrings interface, controls.itextstrings_moveboundary, tom/ITextStrings::MoveBoundary
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
 - ITextStrings.MoveBoundary
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextStrings::MoveBoundary


## -description


Moves the start boundary of a string, by index, for a selected number of characters.


## -parameters




### -param iString [in]

Type: <b>long</b>

The string index.


### -param cch [in]

Type: <b>long</b>

The selected number of characters to move the boundary.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



The index is relative to the top of the collection, so <i>iString</i> = 0 moves the top string boundary, <i>iString</i> = –1 moves the boundary of the string below the top string, and so on.




## -see-also




<a href="https://msdn.microsoft.com/c878d0db-ac13-4ac9-8601-d1c1ba76cd85">ITextStrings</a>
 

 

