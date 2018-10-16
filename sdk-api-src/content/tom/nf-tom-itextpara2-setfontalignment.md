---
UID: NF:tom.ITextPara2.SetFontAlignment
title: ITextPara2::SetFontAlignment
author: windows-sdk-content
description: Sets the paragraph font alignment for Chinese, Japanese, Korean text.
old-location: controls\itextpara2_setfontalignment.htm
tech.root: controls
ms.assetid: 2ed1f7f2-9523-4dda-bac0-c1eb3d217102
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: ITextPara2 interface [Windows Controls],SetFontAlignment method, ITextPara2.SetFontAlignment, ITextPara2::SetFontAlignment, SetFontAlignment, SetFontAlignment method [Windows Controls], SetFontAlignment method [Windows Controls],ITextPara2 interface, controls.itextpara2_setfontalignment, tom/ITextPara2::SetFontAlignment
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
 - ITextPara2.SetFontAlignment
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextPara2::SetFontAlignment


## -description


Sets the paragraph font alignment for Chinese, Japanese, Korean text.  



## -parameters




### -param Value [in]

Type: <b>long</b>

The paragraph font alignment. It can be one of the following values.


<table>
<tr>
<th>Font Alignment States</th>
</tr>
<tr>
<td><a href="tomconstants.htm">tomFontAlignmentAuto</a> (default)</td>
</tr>
<tr>
<td><a href="tomconstants.htm">tomFontAlignmentTop</a></td>
</tr>
<tr>
<td><a href="tomconstants.htm">tomFontAlignmentBaseline</a></td>
</tr>
<tr>
<td><a href="tomconstants.htm">tomFontAlignmentBottom</a></td>
</tr>
<tr>
<td><a href="tomconstants.htm">tomFontAlignmentCenter</a></td>
</tr>
</table>
 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/31a0849f-c651-4178-b1ff-a4333bcde5d9">ITextPara2</a>



<a href="https://msdn.microsoft.com/1064c033-2ae0-46ec-a670-603edd673e87">ITextPara2::GetFontAlignment</a>
 

 

