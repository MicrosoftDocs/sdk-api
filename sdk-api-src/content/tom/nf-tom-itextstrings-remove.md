---
UID: NF:tom.ITextStrings.Remove
title: ITextStrings::Remove
author: windows-sdk-content
description: Removes a string from a string collection, starting at an index.
old-location: controls\itextstrings_remove.htm
tech.root: controls
ms.assetid: 1909e8b6-ee18-4d17-87cf-29bb3553bb25
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: ITextStrings interface [Windows Controls],Remove method, ITextStrings.Remove, ITextStrings::Remove, Remove, Remove method [Windows Controls], Remove method [Windows Controls],ITextStrings interface, controls.itextstrings_remove, tom/ITextStrings::Remove
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
 - ITextStrings.Remove
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- tom.h
: 
- ITextStrings.Remove
: 
---

# ITextStrings::Remove


## -description


Removes a string from a string collection, starting at an index. 


## -parameters




### -param iString [in]

Type: <b>long</b>

The string index.


### -param cString [in]

Type: <b>long</b>

The count of strings to remove.


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
</table>
 




## -remarks



The index is relative to the top of the collection, so <i>iString</i> = 0 removes the top string (<i>cString</i> must be 1), <i>iString</i> = –1 removes the one below the top string (and the top string if <i>cString</i> = 2), and so on.




## -see-also




<a href="https://msdn.microsoft.com/c878d0db-ac13-4ac9-8601-d1c1ba76cd85">ITextStrings</a>
 

 

