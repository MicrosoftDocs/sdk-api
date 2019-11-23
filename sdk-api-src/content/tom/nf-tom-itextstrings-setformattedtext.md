---
UID: NF:tom.ITextStrings.SetFormattedText
title: ITextStrings::SetFormattedText (tom.h)

description: Replaces text with formatted text.
old-location: controls\itextstrings_setformattedtext.htm
tech.root: Controls
ms.assetid: 4ebf7b46-8398-4751-b8b3-19e94fdbce87

ms.date: 12/05/2018
ms.keywords: ITextStrings interface [Windows Controls],SetFormattedText method, ITextStrings.SetFormattedText, ITextStrings::SetFormattedText, SetFormattedText, SetFormattedText method [Windows Controls], SetFormattedText method [Windows Controls],ITextStrings interface, controls.itextstrings_setformattedtext, tom/ITextStrings::SetFormattedText
ms.topic: method
f1_keywords: 
 - "tom/ITextStrings.SetFormattedText"
dev_langs:
 - c++
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
 - ITextStrings.SetFormattedText
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITextStrings::SetFormattedText


## -description


Replaces text with formatted text.


## -parameters




### -param pRangeD [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/tom/nn-tom-itextrange2">ITextRange2</a>*</b>

The text to be replaced.


### -param pRangeS [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/tom/nn-tom-itextrange2">ITextRange2</a>*</b>

The formatted text.


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following COM error codes. For more information about COM error codes, see <a href="https://docs.microsoft.com/windows/desktop/com/error-handling-in-com">Error Handling in COM</a>.

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
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/tom/nn-tom-itextstrings">ITextStrings</a>
 

 

