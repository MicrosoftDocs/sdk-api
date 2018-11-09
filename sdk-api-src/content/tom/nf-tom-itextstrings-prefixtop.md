---
UID: NF:tom.ITextStrings.PrefixTop
title: ITextStrings::PrefixTop
author: windows-sdk-content
description: Prefixes a string to the top string in the collection.
old-location: controls\itextstrings_prefixtop.htm
tech.root: controls
ms.assetid: fbdae612-1d6e-4f10-9b55-5ee038f27b79
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: ITextStrings interface [Windows Controls],PrefixTop method, ITextStrings.PrefixTop, ITextStrings::PrefixTop, PrefixTop, PrefixTop method [Windows Controls], PrefixTop method [Windows Controls],ITextStrings interface, controls.itextstrings_prefixtop, tom/ITextStrings::PrefixTop
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
 - ITextStrings.PrefixTop
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextStrings::PrefixTop


## -description


Prefixes a string to the top  string in the collection.


## -parameters




### -param bstr [in]

Type: <b>BSTR</b>

The string to prefix to the collection.


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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/c878d0db-ac13-4ac9-8601-d1c1ba76cd85">ITextStrings</a>
 

 

