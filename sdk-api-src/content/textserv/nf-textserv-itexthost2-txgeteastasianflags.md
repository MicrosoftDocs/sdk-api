---
UID: NF:textserv.ITextHost2.TxGetEastAsianFlags
title: ITextHost2::TxGetEastAsianFlags (textserv.h)
description: Gets whether Input Method Editor (IME) input is allowed and whether the edit styles include ES_SELFIME.
old-location: controls\itexthost2_txgeteastasianflags.htm
tech.root: Controls
ms.assetid: 3D704159-795A-4BD6-B699-EC311D9B780C
ms.date: 12/05/2018
ms.keywords: ES_NOIME, ES_SELFIME, ITextHost2 interface [Windows Controls],TxGetEastAsianFlags method, ITextHost2.TxGetEastAsianFlags, ITextHost2::TxGetEastAsianFlags, TxGetEastAsianFlags, TxGetEastAsianFlags method [Windows Controls], TxGetEastAsianFlags method [Windows Controls],ITextHost2 interface, controls.itexthost2_txgeteastasianflags, textserv/ITextHost2::TxGetEastAsianFlags
f1_keywords:
- textserv/ITextHost2.TxGetEastAsianFlags
dev_langs:
- c++
req.header: textserv.h
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
- ITextHost2.TxGetEastAsianFlags
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITextHost2::TxGetEastAsianFlags


## -description


Gets whether Input Method Editor (IME) input is allowed and whether the edit styles include <a href="https://docs.microsoft.com/windows/desktop/Controls/rich-edit-control-styles">ES_SELFIME</a>.


## -parameters




### -param pFlags

Type: <b>LONG*</b>

The East Asian flags. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ES_NOIME"></a><a id="es_noime"></a><dl>
<dt><b><a href="https://docs.microsoft.com/windows/desktop/Controls/rich-edit-control-styles">ES_NOIME</a></b></dt>
</dl>
</td>
<td width="60%">
IME input is suppressed.

</td>
</tr>
<tr>
<td width="40%"><a id="ES_SELFIME"></a><a id="es_selfime"></a><dl>
<dt><b><a href="https://docs.microsoft.com/windows/desktop/Controls/rich-edit-control-styles">ES_SELFIME</a></b></dt>
</dl>
</td>
<td width="60%">
The rich edit client handles IME imput.

</td>
</tr>
</table>
 


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/textserv/nl-textserv-itexthost2">ITextHost2</a>
 

 

