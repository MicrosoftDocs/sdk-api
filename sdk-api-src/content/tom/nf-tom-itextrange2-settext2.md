---
UID: NF:tom.ITextRange2.SetText2
title: ITextRange2::SetText2
author: windows-sdk-content
description: Sets the text of this range.
old-location: controls\itextrange2_settext2.htm
tech.root: controls
ms.assetid: dd7a8a16-6cb5-40ee-8f5f-e51e68785d93
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITextRange2 interface [Windows Controls],SetText2 method, ITextRange2.SetText2, ITextRange2::SetText2, SetText2, SetText2 method [Windows Controls], SetText2 method [Windows Controls],ITextRange2 interface, controls.itextrange2_settext2, tom/ITextRange2::SetText2, tomCheckTextLimit, tomLanguageTag, tomMathCFCheck, tomUnhide, tomUnicodeBiDi, tomUnlink
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
 - ITextRange2.SetText2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextRange2::SetText2


## -description


Sets the text of this range.


## -parameters




### -param Flags [in]

Type: <b>long</b>

Flags controlling how the text is inserted in the range. The flag can be one of the following values:

<a id="tomUnicodeBiDi"></a>
<a id="tomunicodebidi"></a>
<a id="TOMUNICODEBIDI"></a>


#### tomUnicodeBiDi

<a id="tomMathCFCheck"></a>
<a id="tommathcfcheck"></a>
<a id="TOMMATHCFCHECK"></a>


#### tomMathCFCheck

<a id="tomUnlink"></a>
<a id="tomunlink"></a>
<a id="TOMUNLINK"></a>


#### tomUnlink

<a id="tomUnhide"></a>
<a id="tomunhide"></a>
<a id="TOMUNHIDE"></a>


#### tomUnhide

<a id="tomCheckTextLimit"></a>
<a id="tomchecktextlimit"></a>
<a id="TOMCHECKTEXTLIMIT"></a>


#### tomCheckTextLimit

<a id="tomLanguageTag"></a>
<a id="tomlanguagetag"></a>
<a id="TOMLANGUAGETAG"></a>


#### tomLanguageTag


### -param bstr [in]

Type: <b>BSTR</b>

The new text.


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
 




## -remarks



If the <i>bstr</i> parameter is <b>NULL</b>, the text in the range is deleted. 

This method is similar to <a href="https://msdn.microsoft.com/en-us/library/Bb787831(v=VS.85).aspx">ITextRange:: SetText</a>, but lets the client specify flags that control various insertion options, including the special flag <b>tomLanguageTag</b> to get the BCP-47 language tag for the range. This is an industry standard language tag that may be preferable to <a href="https://msdn.microsoft.com/en-us/library/Bb774167(v=VS.85).aspx">ITextFont::SetLanguageID</a>, which uses a language code identifier (LCID).




## -see-also




<a href="https://msdn.microsoft.com/905f0967-8b99-45ed-a1cc-19d49e919a65">ITextRange2</a>



<a href="https://msdn.microsoft.com/77f39808-b39d-45bb-ba03-3a27d503fe0e">ITextRange2::GetText2</a>
 

 

