---
UID: NF:tom.ITextStrings.SetOpCp
title: ITextStrings::SetOpCp (tom.h)
description: Sets the character position in the source range's story that has desired character formatting attributes.
helpviewer_keywords: ["ITextStrings interface [Windows Controls]","SetOpCp method","ITextStrings.SetOpCp","ITextStrings::SetOpCp","SetOpCp","SetOpCp method [Windows Controls]","SetOpCp method [Windows Controls]","ITextStrings interface","controls.itextstrings_setopcp","tom/ITextStrings::SetOpCp"]
old-location: controls\itextstrings_setopcp.htm
tech.root: Controls
ms.assetid: c869a42a-0937-4051-9cb0-d454255989d2
ms.date: 12/05/2018
ms.keywords: ITextStrings interface [Windows Controls],SetOpCp method, ITextStrings.SetOpCp, ITextStrings::SetOpCp, SetOpCp, SetOpCp method [Windows Controls], SetOpCp method [Windows Controls],ITextStrings interface, controls.itextstrings_setopcp, tom/ITextStrings::SetOpCp
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITextStrings::SetOpCp
 - tom/ITextStrings::SetOpCp
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msftedit.dll
api_name:
 - ITextStrings.SetOpCp
---

# ITextStrings::SetOpCp


## -description

Sets the character position in the source range's story that has desired character formatting attributes.  The <a href="/windows/desktop/api/tom/nf-tom-itextstrings-encodefunction">ITextStrings::EncodeFunction</a> method applies those character formatting attributes to the operators specified by the <i>Char</i>, <i>Char1</i>, and <i>Char2</i> parameters.

## -parameters

### -param iString [in]

Type: <b>long</b>

The index of the string to associate with a character position.

### -param cp [in]

Type: <b>long</b>

The character position in source range's story that has the desired character formatting.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following COM error codes. For more information about COM error codes, see <a href="/windows/desktop/com/error-handling-in-com">Error Handling in COM</a>.

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

<a href="/windows/desktop/api/tom/nn-tom-itextstrings">ITextStrings</a>