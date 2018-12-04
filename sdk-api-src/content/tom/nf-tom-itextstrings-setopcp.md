---
UID: NF:tom.ITextStrings.SetOpCp
title: ITextStrings::SetOpCp
author: windows-sdk-content
description: Sets the character position in the source range's story that has desired character formatting attributes.
old-location: controls\itextstrings_setopcp.htm
tech.root: controls
ms.assetid: c869a42a-0937-4051-9cb0-d454255989d2
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: ITextStrings interface [Windows Controls],SetOpCp method, ITextStrings.SetOpCp, ITextStrings::SetOpCp, SetOpCp, SetOpCp method [Windows Controls], SetOpCp method [Windows Controls],ITextStrings interface, controls.itextstrings_setopcp, tom/ITextStrings::SetOpCp
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
 - ITextStrings.SetOpCp
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextStrings::SetOpCp


## -description


Sets the character position in the source range's story that has desired character formatting attributes.  The <a href="https://msdn.microsoft.com/f22bb343-4fcc-4473-84cc-807011b5a7b0">ITextStrings::EncodeFunction</a> method applies those character formatting attributes to the operators specified by the <i>Char</i>, <i>Char1</i>, and <i>Char2</i> parameters.


## -parameters




### -param iString [in]

Type: <b>long</b>

The index of the string to associate with a character position.


### -param cp [in]

Type: <b>long</b>

The character position in source range's story that has the desired character formatting.


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
 




## -see-also




<a href="https://msdn.microsoft.com/c878d0db-ac13-4ac9-8601-d1c1ba76cd85">ITextStrings</a>
 

 

