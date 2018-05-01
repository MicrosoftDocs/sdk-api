---
UID: NF:tom.ITextStrings.Add
title: ITextStrings::Add method
author: windows-driver-content
description: Adds a string to the end of the collection.
old-location: controls\itextstrings_add.htm
old-project: Controls
ms.assetid: 59630068-e3c7-4c3b-bd89-f1127759f979
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: Add method [Windows Controls], Add method [Windows Controls], ITextStrings interface, Add,ITextStrings.Add, ITextStrings, ITextStrings interface [Windows Controls], Add method, ITextStrings::Add, controls.itextstrings_add, tom/ITextStrings::Add
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
-	ITextStrings.Add
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextStrings::Add method


## -description


Adds a string to the end of the collection.


## -parameters




### -param bstr [in]

Type: <b>BSTR</b>

The string. The value can be <b>NULL</b> for  a null string.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following COM error codes. For more information about COM error codes, see <a href="https://msdn.microsoft.com/15f3ae3e-1794-4948-a7aa-6309a703364b">Error Handling in COM</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory.

</td>
</tr>
</table>
 




## -remarks



Adding an item to the end of a collection is like pushing a parameter onto the stack. 




## -see-also




<a href="https://msdn.microsoft.com/c878d0db-ac13-4ac9-8601-d1c1ba76cd85">ITextStrings</a>
 

 

