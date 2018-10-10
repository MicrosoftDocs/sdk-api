---
UID: NF:tom.ITextStrings.DeleteRange
title: ITextStrings::DeleteRange
author: windows-sdk-content
description: Deletes the contents of a given range.
old-location: controls\itextstrings_deleterange.htm
tech.root: Controls
ms.assetid: 2dd6312a-77ab-4538-a51b-7de49a5457ff
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: DeleteRange, DeleteRange method [Windows Controls], DeleteRange method [Windows Controls],ITextStrings interface, ITextStrings interface [Windows Controls],DeleteRange method, ITextStrings.DeleteRange, ITextStrings::DeleteRange, controls.itextstrings_deleterange, tom/ITextStrings::DeleteRange
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
 - ITextStrings.DeleteRange
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextStrings::DeleteRange


## -description


Deletes the contents of a given range.


## -parameters




### -param pRange [in]

Type: <b><a href="https://msdn.microsoft.com/905f0967-8b99-45ed-a1cc-19d49e919a65">ITextRange2</a>*</b>

The range to delete.


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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Range is not degenerate.

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



If the text selected by the range is not completely contained by the string, the method fails.




## -see-also




<a href="https://msdn.microsoft.com/c878d0db-ac13-4ac9-8601-d1c1ba76cd85">ITextStrings</a>
 

 

