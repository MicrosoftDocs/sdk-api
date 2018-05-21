---
UID: NF:tom.ITextStrings.Append
title: ITextStrings::Append
author: windows-driver-content
description: Appends a string to the string at the specified index in the collection.
old-location: controls\itextstrings_append.htm
old-project: Controls
ms.assetid: e280008b-b41e-43e3-9f16-6fe1f88e10ea
ms.author: windowsdriverdev
ms.date: 5/17/2018
ms.keywords: Append, Append method [Windows Controls], Append method [Windows Controls],ITextStrings interface, ITextStrings interface [Windows Controls],Append method, ITextStrings.Append, ITextStrings::Append, controls.itextstrings_append, tom/ITextStrings::Append
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
-	ITextStrings.Append
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextStrings::Append


## -description


Appends a string to the string at the specified index in the collection.


## -parameters




### -param pRange [in]

Type: <b><a href="https://msdn.microsoft.com/905f0967-8b99-45ed-a1cc-19d49e919a65">ITextRange2</a>*</b>

The string to append.


### -param iString [in]

Type: <b>long</b>

The string index.


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



The index is relative to the top of the collection, so if  <i>iString</i> is equal to 0 the string is inserted at the top. If <i>iString</i> is equal to  –1, it is inserted below the top string, and so on.




## -see-also




<a href="https://msdn.microsoft.com/c878d0db-ac13-4ac9-8601-d1c1ba76cd85">ITextStrings</a>
 

 

