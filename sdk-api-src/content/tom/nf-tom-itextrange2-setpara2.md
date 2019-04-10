---
UID: NF:tom.ITextRange2.SetPara2
title: ITextRange2::SetPara2 (tom.h)
author: windows-sdk-content
description: Sets the paragraph format attributes of a range.
old-location: controls\itextrange2_setpara2.htm
tech.root: Controls
ms.assetid: ffd25a04-27a8-47c0-95a4-d66291971819
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITextRange2 interface [Windows Controls],SetPara2 method, ITextRange2.SetPara2, ITextRange2::SetPara2, SetPara2, SetPara2 method [Windows Controls], SetPara2 method [Windows Controls],ITextRange2 interface, controls.itextrange2_setpara2, tom/ITextRange2::SetPara2
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
 - ITextRange2.SetPara2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextRange2::SetPara2


## -description


Sets the paragraph format attributes of a range.


## -parameters




### -param pPara [in]

Type: <b><a href="https://msdn.microsoft.com/31a0849f-c651-4178-b1ff-a4333bcde5d9">ITextPara2</a>*</b>

The desired paragraph format.


## -returns



Type: <b>HRESULT</b>

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
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
Write access is denied.

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
 




## -see-also




<a href="https://msdn.microsoft.com/905f0967-8b99-45ed-a1cc-19d49e919a65">ITextRange2</a>



<a href="https://msdn.microsoft.com/b20ebe85-f2a6-4a19-8b25-f1f16ebf5627">ITextRange2::GetPara2</a>
 

 

