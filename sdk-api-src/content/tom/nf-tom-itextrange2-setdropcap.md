---
UID: NF:tom.ITextRange2.SetDropCap
title: ITextRange2::SetDropCap
author: windows-sdk-content
description: Sets the drop-cap parameters for the paragraph that contains the current range.
old-location: controls\itextrange2_setdropcap.htm
tech.root: Controls
ms.assetid: 189c1a69-44eb-4de0-8ffc-9a026d9e6f16
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: ITextRange2 interface [Windows Controls],SetDropCap method, ITextRange2.SetDropCap, ITextRange2::SetDropCap, SetDropCap, SetDropCap method [Windows Controls], SetDropCap method [Windows Controls],ITextRange2 interface, controls.itextrange2_setdropcap, tom/ITextRange2::SetDropCap
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: tom.h
req.include-header: Tom.h
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
 - ITextRange2.SetDropCap
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextRange2::SetDropCap


## -description


Not implemented.

Sets the drop-cap parameters for the paragraph that contains the current range.


## -parameters




### -param cLine [in]

Type: <b>long</b>

The count of lines for drop cap. Zero means no drop cap.


### -param Position [in]

Type: <b>long</b>

The position of drop cap. It can be one of the following. <dl>
<dd>tomDropMargin</dd>
<dd>tomDropNone</dd>
<dd>tomDropNormal</dd>
</dl>



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
</table>
 




## -remarks



The current range can be degenerate, or you can select up to the complete drop-cap paragraph. If the range contains more than one paragraph, this method returns <b>E_FAIL</b>.




## -see-also




<a href="https://msdn.microsoft.com/905f0967-8b99-45ed-a1cc-19d49e919a65">ITextRange2</a>



<a href="https://msdn.microsoft.com/c653c002-6708-4813-83ae-1ea578bdcee2">ITextRange2::GetDropCap</a>
 

 

