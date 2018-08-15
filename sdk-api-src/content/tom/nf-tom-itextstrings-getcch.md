---
UID: NF:tom.ITextStrings.GetCch
title: ITextStrings::GetCch
author: windows-sdk-content
description: Gets the count of characters for a selected string index.
old-location: controls\itextstrings_getcch.htm
old-project: controls
ms.assetid: 73b88019-f74b-4345-95f3-9f924c999b8a
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetCch, GetCch method [Windows Controls], GetCch method [Windows Controls],ITextStrings interface, ITextStrings interface [Windows Controls],GetCch method, ITextStrings.GetCch, ITextStrings::GetCch, controls.itextstrings_getcch, tom/ITextStrings::GetCch
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: tom.h
req.include-header: 
req.redist: 
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
 - ITextStrings.GetCch
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextStrings::GetCch


## -description


Gets the count of characters for a selected string index.


## -parameters




### -param iString [in]

Type: <b>long</b>

The string index.


### -param pcch [out]

Type: <b>long*</b>

The string character count.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



The index is relative to the top of the collection, so <i>iString</i> = 0 returns the character count of the top string, <i>iString</i> = –1 returns that for the one below the top string, and so on.




## -see-also




<a href="https://msdn.microsoft.com/c878d0db-ac13-4ac9-8601-d1c1ba76cd85">ITextStrings</a>
 

 

