---
UID: NF:tom.ITextFont2.SetCharRep
title: ITextFont2::SetCharRep (tom.h)
description: Sets the character repertoire (writing system).
helpviewer_keywords: ["ITextFont2 interface [Windows Controls]","SetCharRep method","ITextFont2.SetCharRep","ITextFont2::SetCharRep","SetCharRep","SetCharRep method [Windows Controls]","SetCharRep method [Windows Controls]","ITextFont2 interface","controls.itextfont2_setcharrep","tom/ITextFont2::SetCharRep"]
old-location: controls\itextfont2_setcharrep.htm
tech.root: Controls
ms.assetid: 6c57b5e5-a5c7-416a-851c-fc8ef16b5a9a
ms.date: 12/05/2018
ms.keywords: ITextFont2 interface [Windows Controls],SetCharRep method, ITextFont2.SetCharRep, ITextFont2::SetCharRep, SetCharRep, SetCharRep method [Windows Controls], SetCharRep method [Windows Controls],ITextFont2 interface, controls.itextfont2_setcharrep, tom/ITextFont2::SetCharRep
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
 - ITextFont2::SetCharRep
 - tom/ITextFont2::SetCharRep
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
 - ITextFont2.SetCharRep
---

# ITextFont2::SetCharRep


## -description

Sets the character repertoire (writing system).

## -parameters

### -param Value [in]

Type: <b>long</b>

The new character repertoire. For a list of possible values, see <a href="/windows/desktop/api/tom/nf-tom-itextfont2-getcharrep">ITextFont2::GetCharRep</a>.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextfont2">ITextFont2</a>



<a href="/windows/desktop/api/tom/nf-tom-itextfont2-getcharrep">ITextFont2::GetCharRep</a>